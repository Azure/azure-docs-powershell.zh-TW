---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
ms.openlocfilehash: e2de3546f805e006bd7f48e2ee7f95b8f3347544
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457324"
---
# <span data-ttu-id="4a0af-101">New-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="4a0af-101">New-AzureRmAutomationModule</span></span>

## <span data-ttu-id="4a0af-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4a0af-102">SYNOPSIS</span></span>
<span data-ttu-id="4a0af-103">將模組匯入自動化。</span><span class="sxs-lookup"><span data-stu-id="4a0af-103">Imports a module into Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a0af-104">句法</span><span class="sxs-lookup"><span data-stu-id="4a0af-104">SYNTAX</span></span>

```
New-AzureRmAutomationModule [-Name] <String> -ContentLinkUri <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a0af-105">說明</span><span class="sxs-lookup"><span data-stu-id="4a0af-105">DESCRIPTION</span></span>
<span data-ttu-id="4a0af-106">**新的-AzureRmAutomationModule** Cmdlet 會將模組匯入 Azure 自動化。</span><span class="sxs-lookup"><span data-stu-id="4a0af-106">The **New-AzureRmAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="4a0af-107">這個命令會接受副檔名為 .zip 的壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="4a0af-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="4a0af-108">檔案包含的資料夾包含下列其中一種類型的檔案：</span><span class="sxs-lookup"><span data-stu-id="4a0af-108">The file contains a folder that includes a file that is one of the following types:</span></span> 

- <span data-ttu-id="4a0af-109">wps_2 模組，其副檔名為 psm1 或 .dll</span><span class="sxs-lookup"><span data-stu-id="4a0af-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="4a0af-110">wps_2 的模組資訊清單，副檔名為 psd1。</span><span class="sxs-lookup"><span data-stu-id="4a0af-110">wps_2 module manifest, which has a .psd1 file name extension</span></span>

<span data-ttu-id="4a0af-111">.Zip 檔案的名稱、資料夾的名稱，以及資料夾中的檔案名都必須是相同的名稱。</span><span class="sxs-lookup"><span data-stu-id="4a0af-111">The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>

<span data-ttu-id="4a0af-112">將 .zip 檔案指定為自動化服務可存取的 URL。</span><span class="sxs-lookup"><span data-stu-id="4a0af-112">Specify the .zip file as a URL that the Automation service can access.</span></span>

<span data-ttu-id="4a0af-113">如果您使用這個 Cmdlet 或 Set-AzureRmAutomationModule Cmdlet 將 wps_2 模組匯入自動化，該作業就是非同步作業。</span><span class="sxs-lookup"><span data-stu-id="4a0af-113">If you import a wps_2 module into Automation by using this cmdlet or the Set-AzureRmAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="4a0af-114">不論匯入成功與否，命令都會完成。</span><span class="sxs-lookup"><span data-stu-id="4a0af-114">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="4a0af-115">若要檢查是否成功，請執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="4a0af-115">To check whether it succeeded, run the following command:</span></span>

<span data-ttu-id="4a0af-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span><span class="sxs-lookup"><span data-stu-id="4a0af-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span></span>

<span data-ttu-id="4a0af-117">檢查 **ProvisioningState** 屬性的值是否為 Succeeded。</span><span class="sxs-lookup"><span data-stu-id="4a0af-117">Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="4a0af-118">示例</span><span class="sxs-lookup"><span data-stu-id="4a0af-118">EXAMPLES</span></span>

### <span data-ttu-id="4a0af-119">範例1：匯入模組</span><span class="sxs-lookup"><span data-stu-id="4a0af-119">Example 1: Import a module</span></span>
```
PS C:\>New-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4a0af-120">這個命令會將名為 ContosoModule 的模組匯入到名為 Contoso17 的自動化帳戶中。</span><span class="sxs-lookup"><span data-stu-id="4a0af-120">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="4a0af-121">該模組會儲存在名為 contosostorage 的儲存空間帳戶和名為「模組」的容器中的 Azure blob 中。</span><span class="sxs-lookup"><span data-stu-id="4a0af-121">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="4a0af-122">參數</span><span class="sxs-lookup"><span data-stu-id="4a0af-122">PARAMETERS</span></span>

### <span data-ttu-id="4a0af-123">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4a0af-123">-AutomationAccountName</span></span>
<span data-ttu-id="4a0af-124">指定此 Cmdlet 要匯入模組的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="4a0af-124">Specifies the name of the Automation account for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="4a0af-125">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="4a0af-125">-ContentLinkUri</span></span>
<span data-ttu-id="4a0af-126">模組 zip 封裝的 url。</span><span class="sxs-lookup"><span data-stu-id="4a0af-126">The url to a module zip package.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a0af-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="4a0af-127">-Name</span></span>
<span data-ttu-id="4a0af-128">指定此 Cmdlet 所匯入的模組名稱。</span><span class="sxs-lookup"><span data-stu-id="4a0af-128">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="4a0af-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a0af-129">-ResourceGroupName</span></span>
<span data-ttu-id="4a0af-130">指定此 Cmdlet 要匯入模組的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4a0af-130">Specifies the name of a resource group for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="4a0af-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a0af-131">-DefaultProfile</span></span>
<span data-ttu-id="4a0af-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4a0af-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a0af-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a0af-133">CommonParameters</span></span>
<span data-ttu-id="4a0af-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4a0af-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a0af-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4a0af-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a0af-136">輸入</span><span class="sxs-lookup"><span data-stu-id="4a0af-136">INPUTS</span></span>

## <span data-ttu-id="4a0af-137">輸出</span><span class="sxs-lookup"><span data-stu-id="4a0af-137">OUTPUTS</span></span>

### <span data-ttu-id="4a0af-138">[-Azure. 命令. Model. Module]</span><span class="sxs-lookup"><span data-stu-id="4a0af-138">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="4a0af-139">筆記</span><span class="sxs-lookup"><span data-stu-id="4a0af-139">NOTES</span></span>

## <span data-ttu-id="4a0af-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="4a0af-140">RELATED LINKS</span></span>

[<span data-ttu-id="4a0af-141">AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="4a0af-141">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="4a0af-142">移除-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="4a0af-142">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)

[<span data-ttu-id="4a0af-143">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="4a0af-143">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


