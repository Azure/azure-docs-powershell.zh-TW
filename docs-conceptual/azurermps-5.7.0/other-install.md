---
title: Azure PowerShell 的其他安裝方式
description: 如何不使用 PowerShellGet 來安裝 Azure PowerShell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 7148188603e84efbcd784264de4c78819edf6833
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243713"
---
# <a name="install-azure-powershell-on-windows-with-msi-or-web-platform-installer"></a><span data-ttu-id="dfbef-103">使用 MSI 或 Web Platform Installer 在 Windows 上安裝 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="dfbef-103">Install Azure PowerShell on Windows with MSI or Web Platform Installer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="dfbef-104">本文說明如何使用 MSI 或 Web Platform Installer (WebPI) 在 Windows 上安裝 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="dfbef-104">This article explains how to install Azure PowerShell on Windows using an MSI or Web Platform Installer (WebPI).</span></span>
<span data-ttu-id="dfbef-105">只有在您的系統需要時才使用這些安裝方法。</span><span class="sxs-lookup"><span data-stu-id="dfbef-105">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="dfbef-106">在 Windows 上安裝 Azure PowerShell 的建議方法是使用 PowerShellGet。</span><span class="sxs-lookup"><span data-stu-id="dfbef-106">The recommended way to install Azure PowerShell on Windows is with PowerShellGet.</span></span> <span data-ttu-id="dfbef-107">如需使用 PowerShellGet 安裝 Azure PowerShell 的指示，請參閱[使用 PowerShellGet 安裝 Azure PowerShell](install-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="dfbef-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="dfbef-108">使用 MSI 套件在 Windows 上安裝或更新</span><span class="sxs-lookup"><span data-stu-id="dfbef-108">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="dfbef-109">您可以使用 MSI 檔案 (可從 [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018) 取得) 來安裝 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="dfbef-109">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018).</span></span> <span data-ttu-id="dfbef-110">如果您已利用 MSI 身分安裝舊版的 Azure 模組，安裝程式會自動移除這些模組。</span><span class="sxs-lookup"><span data-stu-id="dfbef-110">If you have installed previous versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="dfbef-111">MSI 套件會在 `${env:ProgramFiles}\WindowsPowerShell\Modules` 中安裝模組。</span><span class="sxs-lookup"><span data-stu-id="dfbef-111">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="dfbef-112">`AzureRM` 和 `Azure` 模組都已安裝。</span><span class="sxs-lookup"><span data-stu-id="dfbef-112">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="dfbef-113">僅在您使用 Azure 傳統部署模型時，才使用 `Azure` 模組。</span><span class="sxs-lookup"><span data-stu-id="dfbef-113">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="dfbef-114">若要開始使用 Azure PowerShell，您必須使用 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) Cmdlet 將 `AzureRM` 載入您目前的 PowerShell 工作階段，然後使用您的 Azure 認證登入。</span><span class="sxs-lookup"><span data-stu-id="dfbef-114">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="dfbef-115">您必須針對每個啟動的新 PowerShell 工作階段重複這些步驟。</span><span class="sxs-lookup"><span data-stu-id="dfbef-115">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="dfbef-116">自動匯入 `AzureRM` 模組需要設定 PowerShell 設定檔，您可以在[關於設定檔](/powershell/module/microsoft.powershell.core/about/about_profiles)中加以了解。</span><span class="sxs-lookup"><span data-stu-id="dfbef-116">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="dfbef-117">若要了解如何在工作階段之間保存您的 Azure 登入，請參閱[在 PowerShell 工作階段之間保存使用者認證](context-persistence.md)。</span><span class="sxs-lookup"><span data-stu-id="dfbef-117">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="dfbef-118">使用 Web Platform Installer 在 Windows 上安裝或更新</span><span class="sxs-lookup"><span data-stu-id="dfbef-118">Install or update on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="dfbef-119">請下載 [Azure PowerShell WebPI 套件](https://aka.ms/webpi-azps)並開始安裝。</span><span class="sxs-lookup"><span data-stu-id="dfbef-119">Download the [Azure PowerShell WebPI package](https://aka.ms/webpi-azps) and start the install.</span></span> <span data-ttu-id="dfbef-120">如果您已從 MSI 或使用 Web PI 安裝舊版的 Azure 模組，安裝程式會自動移除這些模組。</span><span class="sxs-lookup"><span data-stu-id="dfbef-120">If you have installed previous versions of Azure modules from an MSI or with WebPI, the installer automatically removes them.</span></span> <span data-ttu-id="dfbef-121">模組會安裝至 `${env:ProgramFiles}\WindowsPowerShell\Modules`。</span><span class="sxs-lookup"><span data-stu-id="dfbef-121">Modules are installed into `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="dfbef-122">`AzureRM` 和 `Azure` 模組都已安裝。</span><span class="sxs-lookup"><span data-stu-id="dfbef-122">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="dfbef-123">僅在您使用 Azure 傳統部署模型時，才使用 `Azure` 模組。</span><span class="sxs-lookup"><span data-stu-id="dfbef-123">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="dfbef-124">若要開始使用 Azure PowerShell，您必須使用 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) Cmdlet 將 `AzureRM` 載入您目前的 PowerShell 工作階段，然後使用您的 Azure 認證登入。</span><span class="sxs-lookup"><span data-stu-id="dfbef-124">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="dfbef-125">您必須針對每個啟動的新 PowerShell 工作階段重複這些步驟。</span><span class="sxs-lookup"><span data-stu-id="dfbef-125">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="dfbef-126">自動匯入 `AzureRM` 模組需要設定 PowerShell 設定檔，您可以在[關於設定檔](/powershell/module/microsoft.powershell.core/about/about_profiles)中加以了解。</span><span class="sxs-lookup"><span data-stu-id="dfbef-126">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="dfbef-127">若要了解如何在工作階段之間保存您的 Azure 登入，請參閱[在 PowerShell 工作階段之間保存使用者認證](context-persistence.md)。</span><span class="sxs-lookup"><span data-stu-id="dfbef-127">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>
