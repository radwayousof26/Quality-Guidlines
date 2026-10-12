// assets/js/toggles.js
// Toggle behavior for status and activate buttons.
// Supports elements with data-toggle-status / data-toggle-activate
// and also supports legacy classes .btn-inprogress and .csc-btn-activate.

(function () {
  'use strict';

  function makeToggle(el, options) {
    // options: { onText, offText, activeClass, ariaTrueText? }
    if (!el) return;
    el.setAttribute('role', el.getAttribute('role') || 'button');
    el.setAttribute('tabindex', el.getAttribute('tabindex') || '0');
    if (!el.dataset.orig) el.dataset.orig = el.textContent.trim();
    if (!el.hasAttribute('aria-pressed')) el.setAttribute('aria-pressed', 'false');

    function setOn(on) {
      if (on) {
        el.textContent = options.onText || el.dataset.on || el.dataset.done || 'ON';
        el.classList.add(options.activeClass || 'is-active');
        el.setAttribute('aria-pressed', 'true');
      } else {
        // restore original text if offText not provided
        el.textContent = options.offText || el.dataset.off || el.dataset.orig || 'OFF';
        el.classList.remove(options.activeClass || 'is-active');
        el.setAttribute('aria-pressed', 'false');
      }
    }

    function toggle() {
      setOn(el.getAttribute('aria-pressed') !== 'true');
    }

    el.addEventListener('click', function (e) {
      e.preventDefault();
      toggle();
    });

    el.addEventListener('keydown', function (e) {
      if (e.key === 'Enter' || e.key === ' ') {
        e.preventDefault();
        toggle();
      }
    });

    // Expose a method to set state programmatically
    el._setToggle = setOn;
  }

  // data-toggle-status or .btn-inprogress (In Progress <-> Done)
  document.querySelectorAll('[data-toggle-status], .btn-inprogress').forEach(function (btn) {
    // Determine on/off labels
    var onText = btn.dataset.done || 'DONE';
    var offText = btn.dataset.inprogress || 'INPROGRESS';
    makeToggle(btn, { onText: onText, offText: offText, activeClass: 'done' });
  });

  // data-toggle-activate or .csc-btn-activate (ACTIVATE <-> WORKING ON)
  document.querySelectorAll('[data-toggle-activate], .csc-btn-activate').forEach(function (btn) {
    var onText = btn.dataset.working || 'WORKING ON';
    var offText = btn.dataset.orig || btn.textContent.trim() || '▶ ACTIVATE';
    makeToggle(btn, { onText: onText, offText: offText, activeClass: 'active-working' });
  });

  // Optional: if page includes elements that should initialize to a saved state,
  // we can restore them from localStorage. Uncomment and adapt if you'd like.
  /*
  try {
    document.querySelectorAll('[data-toggle-status], .btn-inprogress, [data-toggle-activate], .csc-btn-activate').forEach(function (el, idx) {
      var key = 'togglestate:' + (el.id || el.dataset.toggleKey || ('btn-' + idx));
      var saved = localStorage.getItem(key);
      if (saved === 'true' && el._setToggle) el._setToggle(true);
      // Save on change
      el.addEventListener('click', function () {
        localStorage.setItem(key, el.getAttribute('aria-pressed') === 'true');
      });
    });
  } catch (e) { console.warn('toggles: localStorage unavailable', e); }
  */

})();
