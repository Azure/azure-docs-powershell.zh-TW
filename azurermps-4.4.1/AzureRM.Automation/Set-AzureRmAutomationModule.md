---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationModule.md
ms.openlocfilehash: a0c3693220ab614dcb84d69bc8c17a0ad632a2b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447177"
---
# <span data-ttu-id="1ac19-101">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="1ac19-101">Set-AzureRmAutomationModule</span></span>

## <span data-ttu-id="1ac19-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1ac19-102">SYNOPSIS</span></span>
<span data-ttu-id="1ac19-103">更新自動化中的模組。</span><span class="sxs-lookup"><span data-stu-id="1ac19-103">Updates a module in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ac19-104">句法</span><span class="sxs-lookup"><span data-stu-id="1ac19-104">SYNTAX</span></span>

```
Set-AzureRmAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1ac19-105">說明</span><span class="sxs-lookup"><span data-stu-id="1ac19-105">DESCRIPTION</span></span>
<span data-ttu-id="1ac19-106">**AzureRmAutomationModule** Cmdlet 會更新 Azure 自動化中的模組。</span><span class="sxs-lookup"><span data-stu-id="1ac19-106">The **Set-AzureRmAutomationModule** cmdlet updates a module in Azure Automation.</span></span>
<span data-ttu-id="1ac19-107">這個命令會接受副檔名為 .zip 的壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="1ac19-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="1ac19-108">檔案包含的資料夾包含下列其中一種類型的檔案：</span><span class="sxs-lookup"><span data-stu-id="1ac19-108">The file contains a folder that includes a file that is one of the following types:</span></span> 

- <span data-ttu-id="1ac19-109">wps_2 模組，其副檔名為 psm1 或 .dll</span><span class="sxs-lookup"><span data-stu-id="1ac19-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="1ac19-110">wps_2 的模組資訊清單，副檔名為 psd1。</span><span class="sxs-lookup"><span data-stu-id="1ac19-110">wps_2 module manifest, which has a .psd1 file name extension</span></span>

<span data-ttu-id="1ac19-111">.Zip 檔案的名稱、資料夾的名稱，以及資料夾中的檔案名都必須是相同的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ac19-111">The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>

<span data-ttu-id="1ac19-112">將 .zip 檔案指定為自動化服務可存取的 URL。</span><span class="sxs-lookup"><span data-stu-id="1ac19-112">Specify the .zip file as a URL that the Automation service can access.</span></span>

<span data-ttu-id="1ac19-113">如果您使用這個 Cmdlet 或 New-AzureRmAutomationModule Cmdlet 將 wps_2 模組匯入自動化，該作業就是非同步作業。</span><span class="sxs-lookup"><span data-stu-id="1ac19-113">If you import a wps_2 module into Automation by using this cmdlet or the New-AzureRmAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="1ac19-114">不論匯入成功與否，命令都會完成。</span><span class="sxs-lookup"><span data-stu-id="1ac19-114">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="1ac19-115">若要檢查是否成功，請執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="1ac19-115">To check whether it succeeded, run the following command:</span></span>

<span data-ttu-id="1ac19-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span><span class="sxs-lookup"><span data-stu-id="1ac19-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span></span>

<span data-ttu-id="1ac19-117">檢查 **ProvisioningState** 屬性的值是否為 Succeeded。</span><span class="sxs-lookup"><span data-stu-id="1ac19-117">Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="1ac19-118">示例</span><span class="sxs-lookup"><span data-stu-id="1ac19-118">EXAMPLES</span></span>

### <span data-ttu-id="1ac19-119">範例1：更新模組</span><span class="sxs-lookup"><span data-stu-id="1ac19-119">Example 1: Update a module</span></span>
```
PS C:\>Set-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri ".\ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1ac19-120">這個命令會將名為 ContosoModule 的現有模組更新版本，匯入到名為 Contoso17 的自動化帳戶中。</span><span class="sxs-lookup"><span data-stu-id="1ac19-120">This command imports an updated version of an existing module named ContosoModule into the Automation account named Contoso17.</span></span>

## <span data-ttu-id="1ac19-121">參數</span><span class="sxs-lookup"><span data-stu-id="1ac19-121">PARAMETERS</span></span>

### <span data-ttu-id="1ac19-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1ac19-122">-AutomationAccountName</span></span>
<span data-ttu-id="1ac19-123">指定此 Cmdlet 更新模組的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="1ac19-123">Specifies the name of the Automation account for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="1ac19-124">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="1ac19-124">-ContentLinkUri</span></span>
<span data-ttu-id="1ac19-125">指定包含此 Cmdlet 所匯入之模組新版的 .zip 檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="1ac19-125">Specifies the URL of the .zip file that contains the new version of a module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="1ac19-126">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="1ac19-126">-ContentLinkVersion</span></span>
<span data-ttu-id="1ac19-127">指定此 Cmdlet 更新自動化的模組版本。</span><span class="sxs-lookup"><span data-stu-id="1ac19-127">Specifies the version of the module to which this cmdlet updates Automation.</span></span>

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

### <span data-ttu-id="1ac19-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="1ac19-128">-Name</span></span>
<span data-ttu-id="1ac19-129">指定此 Cmdlet 所匯入的模組名稱。</span><span class="sxs-lookup"><span data-stu-id="1ac19-129">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="1ac19-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ac19-130">-ResourceGroupName</span></span>
<span data-ttu-id="1ac19-131">指定此 Cmdlet 更新模組的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ac19-131">Specifies the name of a resource group for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="1ac19-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ac19-132">-DefaultProfile</span></span>
<span data-ttu-id="1ac19-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1ac19-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ac19-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ac19-134">CommonParameters</span></span>
<span data-ttu-id="1ac19-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1ac19-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ac19-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1ac19-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ac19-137">輸入</span><span class="sxs-lookup"><span data-stu-id="1ac19-137">INPUTS</span></span>

## <span data-ttu-id="1ac19-138">輸出</span><span class="sxs-lookup"><span data-stu-id="1ac19-138">OUTPUTS</span></span>

### <span data-ttu-id="1ac19-139">[-Azure. 命令. Model. Module]</span><span class="sxs-lookup"><span data-stu-id="1ac19-139">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="1ac19-140">筆記</span><span class="sxs-lookup"><span data-stu-id="1ac19-140">NOTES</span></span>

## <span data-ttu-id="1ac19-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="1ac19-141">RELATED LINKS</span></span>

[<span data-ttu-id="1ac19-142">AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="1ac19-142">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="1ac19-143">新-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="1ac19-143">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="1ac19-144">移除-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="1ac19-144">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)


