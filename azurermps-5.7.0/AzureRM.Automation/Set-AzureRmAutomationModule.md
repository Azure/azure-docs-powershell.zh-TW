---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationModule.md
ms.openlocfilehash: 7bec79c2c2c4bdc794b1d3b260cad53d82fa5d4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454752"
---
# <span data-ttu-id="279ba-101">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="279ba-101">Set-AzureRmAutomationModule</span></span>

## <span data-ttu-id="279ba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="279ba-102">SYNOPSIS</span></span>
<span data-ttu-id="279ba-103">更新自動化中的模組。</span><span class="sxs-lookup"><span data-stu-id="279ba-103">Updates a module in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="279ba-104">句法</span><span class="sxs-lookup"><span data-stu-id="279ba-104">SYNTAX</span></span>

```
Set-AzureRmAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="279ba-105">說明</span><span class="sxs-lookup"><span data-stu-id="279ba-105">DESCRIPTION</span></span>
<span data-ttu-id="279ba-106">**AzureRmAutomationModule** Cmdlet 會更新 Azure 自動化中的模組。</span><span class="sxs-lookup"><span data-stu-id="279ba-106">The **Set-AzureRmAutomationModule** cmdlet updates a module in Azure Automation.</span></span>
<span data-ttu-id="279ba-107">這個命令會接受副檔名為 .zip 的壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="279ba-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="279ba-108">檔案包含的資料夾包含下列其中一種類型的檔案：</span><span class="sxs-lookup"><span data-stu-id="279ba-108">The file contains a folder that includes a file that is one of the following types:</span></span> 

- <span data-ttu-id="279ba-109">wps_2 模組，其副檔名為 psm1 或 .dll</span><span class="sxs-lookup"><span data-stu-id="279ba-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="279ba-110">wps_2 的模組資訊清單，副檔名為 psd1。</span><span class="sxs-lookup"><span data-stu-id="279ba-110">wps_2 module manifest, which has a .psd1 file name extension</span></span>

<span data-ttu-id="279ba-111">.Zip 檔案的名稱、資料夾的名稱，以及資料夾中的檔案名都必須是相同的名稱。</span><span class="sxs-lookup"><span data-stu-id="279ba-111">The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>

<span data-ttu-id="279ba-112">將 .zip 檔案指定為自動化服務可存取的 URL。</span><span class="sxs-lookup"><span data-stu-id="279ba-112">Specify the .zip file as a URL that the Automation service can access.</span></span>

<span data-ttu-id="279ba-113">如果您使用這個 Cmdlet 或 New-AzureRmAutomationModule Cmdlet 將 wps_2 模組匯入自動化，該作業就是非同步作業。</span><span class="sxs-lookup"><span data-stu-id="279ba-113">If you import a wps_2 module into Automation by using this cmdlet or the New-AzureRmAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="279ba-114">不論匯入成功與否，命令都會完成。</span><span class="sxs-lookup"><span data-stu-id="279ba-114">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="279ba-115">若要檢查是否成功，請執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="279ba-115">To check whether it succeeded, run the following command:</span></span>

<span data-ttu-id="279ba-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span><span class="sxs-lookup"><span data-stu-id="279ba-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span></span>

<span data-ttu-id="279ba-117">檢查 **ProvisioningState** 屬性的值是否為 Succeeded。</span><span class="sxs-lookup"><span data-stu-id="279ba-117">Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="279ba-118">示例</span><span class="sxs-lookup"><span data-stu-id="279ba-118">EXAMPLES</span></span>

### <span data-ttu-id="279ba-119">範例1：更新模組</span><span class="sxs-lookup"><span data-stu-id="279ba-119">Example 1: Update a module</span></span>
```
PS C:\>Set-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="279ba-120">這個命令會將名為 ContosoModule 的現有模組更新版本，匯入到名為 Contoso17 的自動化帳戶中。</span><span class="sxs-lookup"><span data-stu-id="279ba-120">This command imports an updated version of an existing module named ContosoModule into the Automation account named Contoso17.</span></span>  <span data-ttu-id="279ba-121">該模組會儲存在名為 contosostorage 的儲存空間帳戶和名為「模組」的容器中的 Azure blob 中。</span><span class="sxs-lookup"><span data-stu-id="279ba-121">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="279ba-122">參數</span><span class="sxs-lookup"><span data-stu-id="279ba-122">PARAMETERS</span></span>

### <span data-ttu-id="279ba-123">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="279ba-123">-AutomationAccountName</span></span>
<span data-ttu-id="279ba-124">指定此 Cmdlet 更新模組的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="279ba-124">Specifies the name of the Automation account for which this cmdlet updates a module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="279ba-125">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="279ba-125">-ContentLinkUri</span></span>
<span data-ttu-id="279ba-126">指定包含此 Cmdlet 所匯入之模組新版的 .zip 檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="279ba-126">Specifies the URL of the .zip file that contains the new version of a module that this cmdlet imports.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="279ba-127">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="279ba-127">-ContentLinkVersion</span></span>
<span data-ttu-id="279ba-128">指定此 Cmdlet 更新自動化的模組版本。</span><span class="sxs-lookup"><span data-stu-id="279ba-128">Specifies the version of the module to which this cmdlet updates Automation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="279ba-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="279ba-129">-DefaultProfile</span></span>
<span data-ttu-id="279ba-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="279ba-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="279ba-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="279ba-131">-Name</span></span>
<span data-ttu-id="279ba-132">指定此 Cmdlet 所匯入的模組名稱。</span><span class="sxs-lookup"><span data-stu-id="279ba-132">Specifies the name of the module that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="279ba-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="279ba-133">-ResourceGroupName</span></span>
<span data-ttu-id="279ba-134">指定此 Cmdlet 更新模組的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="279ba-134">Specifies the name of a resource group for which this cmdlet updates a module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="279ba-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="279ba-135">CommonParameters</span></span>
<span data-ttu-id="279ba-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="279ba-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="279ba-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="279ba-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="279ba-138">輸入</span><span class="sxs-lookup"><span data-stu-id="279ba-138">INPUTS</span></span>

### <span data-ttu-id="279ba-139">所有</span><span class="sxs-lookup"><span data-stu-id="279ba-139">None</span></span>
<span data-ttu-id="279ba-140">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="279ba-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="279ba-141">輸出</span><span class="sxs-lookup"><span data-stu-id="279ba-141">OUTPUTS</span></span>

### <span data-ttu-id="279ba-142">[-Azure. 命令. Model. Module]</span><span class="sxs-lookup"><span data-stu-id="279ba-142">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="279ba-143">筆記</span><span class="sxs-lookup"><span data-stu-id="279ba-143">NOTES</span></span>

## <span data-ttu-id="279ba-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="279ba-144">RELATED LINKS</span></span>

[<span data-ttu-id="279ba-145">AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="279ba-145">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="279ba-146">新-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="279ba-146">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="279ba-147">移除-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="279ba-147">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)

