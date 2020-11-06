---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
ms.openlocfilehash: 0ddfbd8aceeb26a4f40fcf104919fa9b67b39aa3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444040"
---
# <span data-ttu-id="fa4e2-101">New-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="fa4e2-101">New-AzureRmAutomationModule</span></span>

## <span data-ttu-id="fa4e2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fa4e2-102">SYNOPSIS</span></span>
<span data-ttu-id="fa4e2-103">將模組匯入自動化。</span><span class="sxs-lookup"><span data-stu-id="fa4e2-103">Imports a module into Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa4e2-104">句法</span><span class="sxs-lookup"><span data-stu-id="fa4e2-104">SYNTAX</span></span>

```
New-AzureRmAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa4e2-105">說明</span><span class="sxs-lookup"><span data-stu-id="fa4e2-105">DESCRIPTION</span></span>
<span data-ttu-id="fa4e2-106">**新的-AzureRmAutomationModule** Cmdlet 會將模組匯入 Azure 自動化。</span><span class="sxs-lookup"><span data-stu-id="fa4e2-106">The **New-AzureRmAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="fa4e2-107">這個命令會接受副檔名為 .zip 的壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="fa4e2-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="fa4e2-108">檔案包含的資料夾包含下列其中一種類型的檔案：</span><span class="sxs-lookup"><span data-stu-id="fa4e2-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="fa4e2-109">wps_2 模組，其副檔名為 psm1 或 .dll</span><span class="sxs-lookup"><span data-stu-id="fa4e2-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="fa4e2-110">wps_2 包含副檔名 psd1 的模組資訊清單是 .zip 檔案的名稱、資料夾的名稱，以及資料夾中的檔案名都必須是相同的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa4e2-110">wps_2 module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="fa4e2-111">將 .zip 檔案指定為自動化服務可存取的 URL。</span><span class="sxs-lookup"><span data-stu-id="fa4e2-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="fa4e2-112">如果您使用這個 Cmdlet 或 Set-AzureRmAutomationModule Cmdlet 將 wps_2 模組匯入自動化，該作業就是非同步作業。</span><span class="sxs-lookup"><span data-stu-id="fa4e2-112">If you import a wps_2 module into Automation by using this cmdlet or the Set-AzureRmAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="fa4e2-113">不論匯入成功與否，命令都會完成。</span><span class="sxs-lookup"><span data-stu-id="fa4e2-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="fa4e2-114">若要檢查是否成功，請執行下列命令： `PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name ` ModuleName 檢查 **ProvisioningState** 屬性的值是否為 succeeded。</span><span class="sxs-lookup"><span data-stu-id="fa4e2-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="fa4e2-115">示例</span><span class="sxs-lookup"><span data-stu-id="fa4e2-115">EXAMPLES</span></span>

### <span data-ttu-id="fa4e2-116">範例1：匯入模組</span><span class="sxs-lookup"><span data-stu-id="fa4e2-116">Example 1: Import a module</span></span>
```
PS C:\>New-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="fa4e2-117">這個命令會將名為 ContosoModule 的模組匯入到名為 Contoso17 的自動化帳戶中。</span><span class="sxs-lookup"><span data-stu-id="fa4e2-117">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="fa4e2-118">該模組會儲存在名為 contosostorage 的儲存空間帳戶和名為「模組」的容器中的 Azure blob 中。</span><span class="sxs-lookup"><span data-stu-id="fa4e2-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="fa4e2-119">參數</span><span class="sxs-lookup"><span data-stu-id="fa4e2-119">PARAMETERS</span></span>

### <span data-ttu-id="fa4e2-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fa4e2-120">-AutomationAccountName</span></span>
<span data-ttu-id="fa4e2-121">指定此 Cmdlet 要匯入模組的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="fa4e2-121">Specifies the name of the Automation account for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="fa4e2-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="fa4e2-122">-ContentLinkUri</span></span>
<span data-ttu-id="fa4e2-123">模組 zip 封裝的 url</span><span class="sxs-lookup"><span data-stu-id="fa4e2-123">The url to a module zip package</span></span>

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

### <span data-ttu-id="fa4e2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa4e2-124">-DefaultProfile</span></span>
<span data-ttu-id="fa4e2-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="fa4e2-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa4e2-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="fa4e2-126">-Name</span></span>
<span data-ttu-id="fa4e2-127">指定此 Cmdlet 所匯入的模組名稱。</span><span class="sxs-lookup"><span data-stu-id="fa4e2-127">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="fa4e2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa4e2-128">-ResourceGroupName</span></span>
<span data-ttu-id="fa4e2-129">指定此 Cmdlet 要匯入模組的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa4e2-129">Specifies the name of a resource group for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="fa4e2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa4e2-130">CommonParameters</span></span>
<span data-ttu-id="fa4e2-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fa4e2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa4e2-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fa4e2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa4e2-133">輸入</span><span class="sxs-lookup"><span data-stu-id="fa4e2-133">INPUTS</span></span>

### <span data-ttu-id="fa4e2-134">System.object</span><span class="sxs-lookup"><span data-stu-id="fa4e2-134">System.String</span></span>

### <span data-ttu-id="fa4e2-135">系統 Uri</span><span class="sxs-lookup"><span data-stu-id="fa4e2-135">System.Uri</span></span>

## <span data-ttu-id="fa4e2-136">輸出</span><span class="sxs-lookup"><span data-stu-id="fa4e2-136">OUTPUTS</span></span>

### <span data-ttu-id="fa4e2-137">[-Azure. 命令. Model. Module]</span><span class="sxs-lookup"><span data-stu-id="fa4e2-137">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="fa4e2-138">筆記</span><span class="sxs-lookup"><span data-stu-id="fa4e2-138">NOTES</span></span>

## <span data-ttu-id="fa4e2-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="fa4e2-139">RELATED LINKS</span></span>

[<span data-ttu-id="fa4e2-140">AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="fa4e2-140">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="fa4e2-141">移除-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="fa4e2-141">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)

[<span data-ttu-id="fa4e2-142">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="fa4e2-142">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


