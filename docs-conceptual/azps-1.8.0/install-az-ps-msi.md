---
title: 使用 MSI 安裝 Azure PowerShell
description: 如何使用 MSI，但不使用 PowerShellGet 來安裝 Azure PowerShell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/22/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 7e36765f34a689640e1ed82f5fa221e71d3e08ec
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "89244206"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a><span data-ttu-id="035e2-103">使用 MSI 在 Windows 上安裝 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="035e2-103">Install Azure PowerShell on Windows with MSI</span></span>

<span data-ttu-id="035e2-104">本文說明如何使用 MSI 安裝程式在 Windows 上安裝 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="035e2-104">This article explains how to install Azure PowerShell on Windows using an MSI installer.</span></span> <span data-ttu-id="035e2-105">MSI 安裝程式是針對 PowerShell 資源庫可能受防火牆封鎖，或需要離線安裝程式的環境所提供。</span><span class="sxs-lookup"><span data-stu-id="035e2-105">The MSI installer is provided for environments where the PowerShell Gallery may be blocked by a firewall, or an offline installer is needed.</span></span> <span data-ttu-id="035e2-106">建議使用 PowerShellGet 來安裝 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="035e2-106">The recommended way to install Azure PowerShell is with PowerShellGet.</span></span> <span data-ttu-id="035e2-107">如需使用 PowerShellGet 安裝 Azure PowerShell 的指示，請參閱[使用 PowerShellGet 安裝 Azure PowerShell](install-az-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="035e2-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-az-ps.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="035e2-108">需求</span><span class="sxs-lookup"><span data-stu-id="035e2-108">Requirements</span></span>

<span data-ttu-id="035e2-109">Windows 上的 MSI 安裝程式僅用於安裝適用於 PowerShell 5.1 的 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="035e2-109">The MSI installer on Windows is designed to install Azure PowerShell for PowerShell 5.1 only.</span></span> <span data-ttu-id="035e2-110">若要在非 Windows 平台或較新版本的 PowerShell 上安裝，請[以 PowerShellGet 安裝](install-az-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="035e2-110">For installation on non-Windows platforms or later versions of PowerShell, [Install with PowerShellGet](install-az-ps.md).</span></span> <span data-ttu-id="035e2-111">若要檢查 PowerShell 版本，請執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="035e2-111">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="035e2-112">若要在 PowerShell 5.1 中使用 Azure PowerShell，您需要：</span><span class="sxs-lookup"><span data-stu-id="035e2-112">To use Azure PowerShell in PowerShell 5.1, you need to:</span></span>

1. <span data-ttu-id="035e2-113">視需要更新至 [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell)。</span><span class="sxs-lookup"><span data-stu-id="035e2-113">Update to [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="035e2-114">如果您是在 Windows 10 上，則已安裝 PowerShell 5.1。</span><span class="sxs-lookup"><span data-stu-id="035e2-114">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="035e2-115">安裝 [.NET Framework 4.7.2 或更新版本](/dotnet/framework/install)。</span><span class="sxs-lookup"><span data-stu-id="035e2-115">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="035e2-116">使用 MSI 套件在 Windows 上安裝或更新</span><span class="sxs-lookup"><span data-stu-id="035e2-116">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="035e2-117">可從 [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v1.8.0-April2019)取得 Azure PowerShell 的 MSI 套件。</span><span class="sxs-lookup"><span data-stu-id="035e2-117">The MSI package for Azure PowerShell is available from [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v1.8.0-April2019).</span></span> <span data-ttu-id="035e2-118">如果您已使用 MSI 安裝舊版的 Azure PowerShell，安裝程式會自動移除這些模組。</span><span class="sxs-lookup"><span data-stu-id="035e2-118">If you have installed earlier versions of Azure PowerShell using the MSI, the installer automatically removes them.</span></span> <span data-ttu-id="035e2-119">MSI 套件會在 `${env:ProgramFiles}\WindowsPowerShell\Modules` 中安裝模組。</span><span class="sxs-lookup"><span data-stu-id="035e2-119">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span>

<span data-ttu-id="035e2-120">若要開始使用 Azure PowerShell，請使用您的 Azure 認證登入。</span><span class="sxs-lookup"><span data-stu-id="035e2-120">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzAccount
```

> [!NOTE]
> <span data-ttu-id="035e2-121">如果您已停用自動載入模組功能，則必須透過 `Import-Module Az` 來手動匯入模組。</span><span class="sxs-lookup"><span data-stu-id="035e2-121">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="035e2-122">因為模組的結構化方式，可能需要稍等一分鐘。</span><span class="sxs-lookup"><span data-stu-id="035e2-122">Because of the way the module is structured, this can take up to a minute.</span></span>

<span data-ttu-id="035e2-123">您必須針對每個啟動的新 PowerShell 工作階段重複此步驟。</span><span class="sxs-lookup"><span data-stu-id="035e2-123">You'll need to repeat this step for every new PowerShell session you start.</span></span> <span data-ttu-id="035e2-124">若要了解如何在 PowerShell 工作階段之間保存您的 Azure 登入，請參閱[在 PowerShell 工作階段之間保存使用者認證](context-persistence.md)。</span><span class="sxs-lookup"><span data-stu-id="035e2-124">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="035e2-125">提供意見反應</span><span class="sxs-lookup"><span data-stu-id="035e2-125">Provide feedback</span></span>

<span data-ttu-id="035e2-126">如果您發現 Azure PowerShell 有錯誤，請[在 GitHub 上提出問題](https://github.com/Azure/azure-powershell/issues)。</span><span class="sxs-lookup"><span data-stu-id="035e2-126">If you find a bug in Azure PowerShell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="035e2-127">若要從命令列提供意見反應，請使用 [Send-Feedback](/powershell/module/az.accounts/send-feedback) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="035e2-127">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="035e2-128">後續步驟</span><span class="sxs-lookup"><span data-stu-id="035e2-128">Next Steps</span></span>

<span data-ttu-id="035e2-129">若要深入了解 Azure PowerShell 模組和其功能，請參閱[開始使用 Azure PowerShell](get-started-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="035e2-129">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span> <span data-ttu-id="035e2-130">如果您熟悉 Azure PowerShell 且需要從 AzureRM 遷移，請參閱[從 AzureRM 遷移至 Az](migrate-from-azurerm-to-az.md)。</span><span class="sxs-lookup"><span data-stu-id="035e2-130">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
