---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
ms.openlocfilehash: 475c4ab3105aa8ae01543c0f3674d5d119604a2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916654"
---
# <span data-ttu-id="66509-101">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="66509-101">Set-AzAutomationModule</span></span>

## <span data-ttu-id="66509-102">簡介</span><span class="sxs-lookup"><span data-stu-id="66509-102">SYNOPSIS</span></span>
<span data-ttu-id="66509-103">更新自動化中的模組。</span><span class="sxs-lookup"><span data-stu-id="66509-103">Updates a module in Automation.</span></span>

## <span data-ttu-id="66509-104">語法</span><span class="sxs-lookup"><span data-stu-id="66509-104">SYNTAX</span></span>

```
Set-AzAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="66509-105">描述</span><span class="sxs-lookup"><span data-stu-id="66509-105">DESCRIPTION</span></span>
<span data-ttu-id="66509-106">**Set-AzAutomationModule** Cmdlet 會更新 Azure Automation 中的模組。</span><span class="sxs-lookup"><span data-stu-id="66509-106">The **Set-AzAutomationModule** cmdlet updates a module in Azure Automation.</span></span>
<span data-ttu-id="66509-107">此命令接受副檔名為 .zip 的壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="66509-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="66509-108">檔案包含的資料夾包含下列其中一種類型的檔案：</span><span class="sxs-lookup"><span data-stu-id="66509-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="66509-109">wps_2模組，副檔名為 .psm1 或 .dll</span><span class="sxs-lookup"><span data-stu-id="66509-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="66509-110">wps_2模組清單，其副檔名為 .psd1.ZIP 檔案名、資料夾名稱，以及資料夾中的檔案名必須相同。</span><span class="sxs-lookup"><span data-stu-id="66509-110">wps_2 module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="66509-111">將 .zip 檔案指定為自動化服務可存取的 URL。</span><span class="sxs-lookup"><span data-stu-id="66509-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="66509-112">如果您使用此 Cmdlet 或 wps_2 Cmdlet 將模組New-AzAutomationModule自動化，則作業是非同步。</span><span class="sxs-lookup"><span data-stu-id="66509-112">If you import a wps_2 module into Automation by using this cmdlet or the New-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="66509-113">無論成功或失敗，命令都完成。</span><span class="sxs-lookup"><span data-stu-id="66509-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="66509-114">若要檢查是否成功，請執行下列命令 `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ：ModuleName 檢查 **ProvisioningState** 屬性中的成功值。</span><span class="sxs-lookup"><span data-stu-id="66509-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="66509-115">例子</span><span class="sxs-lookup"><span data-stu-id="66509-115">EXAMPLES</span></span>

### <span data-ttu-id="66509-116">範例 1：更新模組</span><span class="sxs-lookup"><span data-stu-id="66509-116">Example 1: Update a module</span></span>
```
PS C:\>Set-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="66509-117">此命令會將名為 ContosoModule 的現有模組更新版本，導入名為 Contoso17 的自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="66509-117">This command imports an updated version of an existing module named ContosoModule into the Automation account named Contoso17.</span></span>  <span data-ttu-id="66509-118">模組會儲存在 Azure Blob 中名為 contosostorage 的儲存帳戶和名為模組的容器。</span><span class="sxs-lookup"><span data-stu-id="66509-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="66509-119">參數</span><span class="sxs-lookup"><span data-stu-id="66509-119">PARAMETERS</span></span>

### <span data-ttu-id="66509-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="66509-120">-AutomationAccountName</span></span>
<span data-ttu-id="66509-121">指定此 Cmdlet 更新模組的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="66509-121">Specifies the name of the Automation account for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="66509-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="66509-122">-ContentLinkUri</span></span>
<span data-ttu-id="66509-123">指定包含此 Cmdlet 所導入模組新版本的 .zip 檔案 URL。</span><span class="sxs-lookup"><span data-stu-id="66509-123">Specifies the URL of the .zip file that contains the new version of a module that this cmdlet imports.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66509-124">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="66509-124">-ContentLinkVersion</span></span>
<span data-ttu-id="66509-125">指定此 Cmdlet 更新自動化的模組版本。</span><span class="sxs-lookup"><span data-stu-id="66509-125">Specifies the version of the module to which this cmdlet updates Automation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66509-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66509-126">-DefaultProfile</span></span>
<span data-ttu-id="66509-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="66509-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66509-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="66509-128">-Name</span></span>
<span data-ttu-id="66509-129">指定此 Cmdlet 所導入模組的名稱。</span><span class="sxs-lookup"><span data-stu-id="66509-129">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="66509-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66509-130">-ResourceGroupName</span></span>
<span data-ttu-id="66509-131">指定此 Cmdlet 更新模組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="66509-131">Specifies the name of a resource group for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="66509-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66509-132">CommonParameters</span></span>
<span data-ttu-id="66509-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="66509-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66509-134">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="66509-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66509-135">輸入</span><span class="sxs-lookup"><span data-stu-id="66509-135">INPUTS</span></span>

### <span data-ttu-id="66509-136">System.String</span><span class="sxs-lookup"><span data-stu-id="66509-136">System.String</span></span>

### <span data-ttu-id="66509-137">System.Uri</span><span class="sxs-lookup"><span data-stu-id="66509-137">System.Uri</span></span>

## <span data-ttu-id="66509-138">輸出</span><span class="sxs-lookup"><span data-stu-id="66509-138">OUTPUTS</span></span>

### <span data-ttu-id="66509-139">Microsoft.Azure.Commands.Automation.Model.Module</span><span class="sxs-lookup"><span data-stu-id="66509-139">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="66509-140">筆記</span><span class="sxs-lookup"><span data-stu-id="66509-140">NOTES</span></span>

## <span data-ttu-id="66509-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="66509-141">RELATED LINKS</span></span>

[<span data-ttu-id="66509-142">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="66509-142">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="66509-143">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="66509-143">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="66509-144">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="66509-144">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)


