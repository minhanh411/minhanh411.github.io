/* assets/css/style.css
   Two-column portfolio layout, profile sizing, social icons, and divider under Portfolio
*/

/* Page container */
.page-wrapper {
  max-width: 980px;
  margin: 36px auto;
  padding: 0 20px;
  display: flex;
  gap: 40px;
  box-sizing: border-box;
}

/* Left column (profile) */
.profile-col {
  width: 300px; /* fixed narrow column */
  flex: 0 0 300px;
}

/* Right column (content) */
.content-col {
  flex: 1 1 auto;
  min-width: 0;
}

/* Profile image - force circular and constrained */
.profile-photo {
  max-width: 220px;
  width: 70%;
  height: auto;
  display: block;
  margin: 0 auto 14px auto;
  border-radius: 50%;
  object-fit: cover;
  box-shadow: 0 2px 6px rgba(0,0,0,0.06);
}

/* Name and heading */
.profile-name {
  text-align: center;
  font-size: 26px;
  font-weight: 700;
  color: #1d6fa5; /* similar accent color */
  margin: 8px 0 6px 0;
}

/* Short description under name */
.profile-desc {
  text-align: center;
  color: #666;
  margin-bottom: 12px;
  font-weight: 500;
}

/* Social links row (text) */
p.social-links {
  text-align: center;
  margin-top: 8px;
  margin-bottom: 18px;
  font-weight: 500;
  font-size: 0.95rem;
}

/* Social icon container — if using icon markup */
p.social-icons {
  text-align: center;
  margin-bottom: 14px;
}

/* Icon size and spacing */
.social-icons a {
  text-decoration: none;
  margin: 0 12px;
  display: inline-block;
}
.social-icons i {
  font-size: 22px;
  vertical-align: middle;
  transition: transform .18s ease, opacity .18s ease;
}
.social-icons i:hover { transform: scale(1.15); opacity: .85; }

/* Bio paragraphs in left column */
.profile-bio {
  color: #444;
  line-height: 1.5;
  font-size: 0.95rem;
  margin-top: 10px;
}

/* Portfolio heading with thin rule to the right */
.portfolio-header {
  display: flex;
  align-items: center;
  gap: 18px;
  margin-bottom: 18px;
}

.portfolio-title {
  font-size: 26px;
  font-weight: 700;
  margin: 0;
}

/* Thin rule line — goes across remaining width */
.portfolio-rule {
  height: 1px;
  background: #e3e6e8;
  flex: 1 1 auto;
  border-radius: 1px;
}

/* Project section styles (copy / adapt as needed) */
.project {
  margin-bottom: 26px;
}

.project h3 {
  margin: 0 0 6px 0;
  font-size: 18px;
  font-weight: 700;
}

.project .meta {
  color: #666;
  font-size: 0.92rem;
  margin-bottom: 10px;
}

.project p { color: #444; line-height: 1.55; font-size: 0.95rem; }

/* Images inside project content should be responsive */
.content-col img {
  max-width: 100%;
  height: auto;
  display: block;
  margin: 12px 0;
}

/* Responsive: stack columns on narrow screens */
@media (max-width: 880px) {
  .page-wrapper { flex-direction: column; padding: 0 14px; }
  .profile-col { width: auto; flex: none; }
  .profile-photo { width: 160px; }
  .portfolio-rule { display: none; } /* optional: hide rule on tiny screens */
}
