---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
ms.openlocfilehash: 093a6f61668f40b43d2f228035132c010e31d426
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917105"
---
# <span data-ttu-id="55aec-101">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="55aec-101">New-AzAutomationModule</span></span>

## <span data-ttu-id="55aec-102">簡介</span><span class="sxs-lookup"><span data-stu-id="55aec-102">SYNOPSIS</span></span>
<span data-ttu-id="55aec-103">將模組導入自動化。</span><span class="sxs-lookup"><span data-stu-id="55aec-103">Imports a module into Automation.</span></span>

## <span data-ttu-id="55aec-104">語法</span><span class="sxs-lookup"><span data-stu-id="55aec-104">SYNTAX</span></span>

```
New-AzAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55aec-105">描述</span><span class="sxs-lookup"><span data-stu-id="55aec-105">DESCRIPTION</span></span>
<span data-ttu-id="55aec-106">**New-AzAutomationModule Cmdlet** 將模組導入 Azure Automation。</span><span class="sxs-lookup"><span data-stu-id="55aec-106">The **New-AzAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="55aec-107">此命令接受副檔名為 .zip 的壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="55aec-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="55aec-108">檔案包含的資料夾包含下列其中一種類型的檔案：</span><span class="sxs-lookup"><span data-stu-id="55aec-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="55aec-109">Windows PowerShell 模組，副檔名為 .psm1 或 .dll</span><span class="sxs-lookup"><span data-stu-id="55aec-109">Windows PowerShell module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="55aec-110">Windows PowerShell 模組清單，副檔名為 .psd1.ZIP 檔案名、資料夾名稱，以及資料夾中的檔案名必須相同。</span><span class="sxs-lookup"><span data-stu-id="55aec-110">Windows PowerShell module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="55aec-111">將 .zip 檔案指定為自動化服務可存取的 URL。</span><span class="sxs-lookup"><span data-stu-id="55aec-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="55aec-112">如果您使用此 Cmdlet 或 Cmdlet 將 Windows PowerShell 模組Set-AzAutomationModule自動化，則作業是非同步。</span><span class="sxs-lookup"><span data-stu-id="55aec-112">If you import a Windows PowerShell module into Automation by using this cmdlet or the Set-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="55aec-113">無論成功或失敗，命令都完成。</span><span class="sxs-lookup"><span data-stu-id="55aec-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="55aec-114">若要檢查是否成功，請執行下列命令 `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ：ModuleName 檢查 **ProvisioningState** 屬性中的成功值。</span><span class="sxs-lookup"><span data-stu-id="55aec-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="55aec-115">例子</span><span class="sxs-lookup"><span data-stu-id="55aec-115">EXAMPLES</span></span>

### <span data-ttu-id="55aec-116">範例 1：匯出模組</span><span class="sxs-lookup"><span data-stu-id="55aec-116">Example 1: Import a module</span></span>
```
PS C:\>New-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="55aec-117">此命令會將名為 ContosoModule 的模組，導入名為 Contoso17 的自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="55aec-117">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="55aec-118">模組會儲存在 Azure Blob 中名為 contosostorage 的儲存帳戶和名為模組的容器。</span><span class="sxs-lookup"><span data-stu-id="55aec-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="55aec-119">參數</span><span class="sxs-lookup"><span data-stu-id="55aec-119">PARAMETERS</span></span>

### <span data-ttu-id="55aec-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="55aec-120">-AutomationAccountName</span></span>
<span data-ttu-id="55aec-121">指定此 Cmdlet 所輸入模組的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="55aec-121">Specifies the name of the Automation account for which this cmdlet imports a module.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55aec-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="55aec-122">-ContentLinkUri</span></span>
<span data-ttu-id="55aec-123">模組 zip 封裝的 URL</span><span class="sxs-lookup"><span data-stu-id="55aec-123">The url to a module zip package</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55aec-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55aec-124">-DefaultProfile</span></span>
<span data-ttu-id="55aec-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="55aec-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55aec-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="55aec-126">-Name</span></span>
<span data-ttu-id="55aec-127">指定此 Cmdlet 所導入模組的名稱。</span><span class="sxs-lookup"><span data-stu-id="55aec-127">Specifies the name of the module that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55aec-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55aec-128">-ResourceGroupName</span></span>
<span data-ttu-id="55aec-129">指定此 Cmdlet 所輸入模組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="55aec-129">Specifies the name of a resource group for which this cmdlet imports a module.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55aec-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55aec-130">CommonParameters</span></span>
<span data-ttu-id="55aec-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="55aec-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55aec-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="55aec-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55aec-133">輸入</span><span class="sxs-lookup"><span data-stu-id="55aec-133">INPUTS</span></span>

### <span data-ttu-id="55aec-134">System.String</span><span class="sxs-lookup"><span data-stu-id="55aec-134">System.String</span></span>

### <span data-ttu-id="55aec-135">System.Uri</span><span class="sxs-lookup"><span data-stu-id="55aec-135">System.Uri</span></span>

## <span data-ttu-id="55aec-136">輸出</span><span class="sxs-lookup"><span data-stu-id="55aec-136">OUTPUTS</span></span>

### <span data-ttu-id="55aec-137">Microsoft.Azure.Commands.Automation.Model.Module</span><span class="sxs-lookup"><span data-stu-id="55aec-137">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="55aec-138">筆記</span><span class="sxs-lookup"><span data-stu-id="55aec-138">NOTES</span></span>

## <span data-ttu-id="55aec-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="55aec-139">RELATED LINKS</span></span>

[<span data-ttu-id="55aec-140">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="55aec-140">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="55aec-141">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="55aec-141">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="55aec-142">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="55aec-142">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


