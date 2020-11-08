---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
ms.openlocfilehash: 14cd2a45e87fa5042fbf77d4c37d46211f5793a7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969959"
---
# <span data-ttu-id="943c6-101">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="943c6-101">Set-AzAutomationModule</span></span>

## <span data-ttu-id="943c6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="943c6-102">SYNOPSIS</span></span>
<span data-ttu-id="943c6-103">更新自動化中的模組。</span><span class="sxs-lookup"><span data-stu-id="943c6-103">Updates a module in Automation.</span></span>

## <span data-ttu-id="943c6-104">句法</span><span class="sxs-lookup"><span data-stu-id="943c6-104">SYNTAX</span></span>

```
Set-AzAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="943c6-105">說明</span><span class="sxs-lookup"><span data-stu-id="943c6-105">DESCRIPTION</span></span>
<span data-ttu-id="943c6-106">**AzAutomationModule** Cmdlet 會更新 Azure 自動化中的模組。</span><span class="sxs-lookup"><span data-stu-id="943c6-106">The **Set-AzAutomationModule** cmdlet updates a module in Azure Automation.</span></span>
<span data-ttu-id="943c6-107">這個命令會接受副檔名為 .zip 的壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="943c6-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="943c6-108">檔案包含的資料夾包含下列其中一種類型的檔案：</span><span class="sxs-lookup"><span data-stu-id="943c6-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="943c6-109">wps_2 模組，其副檔名為 psm1 或 .dll</span><span class="sxs-lookup"><span data-stu-id="943c6-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="943c6-110">wps_2 包含副檔名 psd1 的模組資訊清單是 .zip 檔案的名稱、資料夾的名稱，以及資料夾中的檔案名都必須是相同的名稱。</span><span class="sxs-lookup"><span data-stu-id="943c6-110">wps_2 module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="943c6-111">將 .zip 檔案指定為自動化服務可存取的 URL。</span><span class="sxs-lookup"><span data-stu-id="943c6-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="943c6-112">如果您使用這個 Cmdlet 或 New-AzAutomationModule Cmdlet 將 wps_2 模組匯入自動化，該作業就是非同步作業。</span><span class="sxs-lookup"><span data-stu-id="943c6-112">If you import a wps_2 module into Automation by using this cmdlet or the New-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="943c6-113">不論匯入成功與否，命令都會完成。</span><span class="sxs-lookup"><span data-stu-id="943c6-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="943c6-114">若要檢查是否成功，請執行下列命令： `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName 檢查 **ProvisioningState** 屬性的值是否為 succeeded。</span><span class="sxs-lookup"><span data-stu-id="943c6-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="943c6-115">示例</span><span class="sxs-lookup"><span data-stu-id="943c6-115">EXAMPLES</span></span>

### <span data-ttu-id="943c6-116">範例1：更新模組</span><span class="sxs-lookup"><span data-stu-id="943c6-116">Example 1: Update a module</span></span>
```
PS C:\>Set-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="943c6-117">這個命令會將名為 ContosoModule 的現有模組更新版本，匯入到名為 Contoso17 的自動化帳戶中。</span><span class="sxs-lookup"><span data-stu-id="943c6-117">This command imports an updated version of an existing module named ContosoModule into the Automation account named Contoso17.</span></span>  <span data-ttu-id="943c6-118">該模組會儲存在名為 contosostorage 的儲存空間帳戶和名為「模組」的容器中的 Azure blob 中。</span><span class="sxs-lookup"><span data-stu-id="943c6-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="943c6-119">參數</span><span class="sxs-lookup"><span data-stu-id="943c6-119">PARAMETERS</span></span>

### <span data-ttu-id="943c6-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="943c6-120">-AutomationAccountName</span></span>
<span data-ttu-id="943c6-121">指定此 Cmdlet 更新模組的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="943c6-121">Specifies the name of the Automation account for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="943c6-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="943c6-122">-ContentLinkUri</span></span>
<span data-ttu-id="943c6-123">指定包含此 Cmdlet 所匯入之模組新版的 .zip 檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="943c6-123">Specifies the URL of the .zip file that contains the new version of a module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="943c6-124">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="943c6-124">-ContentLinkVersion</span></span>
<span data-ttu-id="943c6-125">指定此 Cmdlet 更新自動化的模組版本。</span><span class="sxs-lookup"><span data-stu-id="943c6-125">Specifies the version of the module to which this cmdlet updates Automation.</span></span>

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

### <span data-ttu-id="943c6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="943c6-126">-DefaultProfile</span></span>
<span data-ttu-id="943c6-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="943c6-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="943c6-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="943c6-128">-Name</span></span>
<span data-ttu-id="943c6-129">指定此 Cmdlet 所匯入的模組名稱。</span><span class="sxs-lookup"><span data-stu-id="943c6-129">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="943c6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="943c6-130">-ResourceGroupName</span></span>
<span data-ttu-id="943c6-131">指定此 Cmdlet 更新模組的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="943c6-131">Specifies the name of a resource group for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="943c6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="943c6-132">CommonParameters</span></span>
<span data-ttu-id="943c6-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="943c6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="943c6-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="943c6-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="943c6-135">輸入</span><span class="sxs-lookup"><span data-stu-id="943c6-135">INPUTS</span></span>

### <span data-ttu-id="943c6-136">System.object</span><span class="sxs-lookup"><span data-stu-id="943c6-136">System.String</span></span>

### <span data-ttu-id="943c6-137">系統 Uri</span><span class="sxs-lookup"><span data-stu-id="943c6-137">System.Uri</span></span>

## <span data-ttu-id="943c6-138">輸出</span><span class="sxs-lookup"><span data-stu-id="943c6-138">OUTPUTS</span></span>

### <span data-ttu-id="943c6-139">[-Azure. 命令. Model. Module]</span><span class="sxs-lookup"><span data-stu-id="943c6-139">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="943c6-140">筆記</span><span class="sxs-lookup"><span data-stu-id="943c6-140">NOTES</span></span>

## <span data-ttu-id="943c6-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="943c6-141">RELATED LINKS</span></span>

[<span data-ttu-id="943c6-142">AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="943c6-142">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="943c6-143">新-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="943c6-143">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="943c6-144">移除-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="943c6-144">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

