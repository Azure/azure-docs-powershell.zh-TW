---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
ms.openlocfilehash: 50a548716019f3b5e80cde4b89ae666f5b6199ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625944"
---
# <span data-ttu-id="f4852-101">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="f4852-101">Get-AzureRmApiManagement</span></span>

## <span data-ttu-id="f4852-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f4852-102">SYNOPSIS</span></span>
<span data-ttu-id="f4852-103">取得清單或特定的 API 管理服務描述。</span><span class="sxs-lookup"><span data-stu-id="f4852-103">Gets a list or a particular API Management Service description.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4852-104">句法</span><span class="sxs-lookup"><span data-stu-id="f4852-104">SYNTAX</span></span>

### <span data-ttu-id="f4852-105">GetBySubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="f4852-105">GetBySubscription (Default)</span></span>
```
Get-AzureRmApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4852-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f4852-106">GetByResourceGroup</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f4852-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="f4852-107">GetByResource</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4852-108">說明</span><span class="sxs-lookup"><span data-stu-id="f4852-108">DESCRIPTION</span></span>
<span data-ttu-id="f4852-109">**AzureRmApiManagement** Cmdlet 會取得 [訂閱] 或 [指定的資源] 群組或特定 API 管理下的所有 API 管理服務清單。</span><span class="sxs-lookup"><span data-stu-id="f4852-109">The **Get-AzureRmApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="f4852-110">示例</span><span class="sxs-lookup"><span data-stu-id="f4852-110">EXAMPLES</span></span>

### <span data-ttu-id="f4852-111">範例1：取得所有 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="f4852-111">Example 1: Get all API Management services</span></span>
```
PS C:\>Get-AzureRmApiManagement
```

<span data-ttu-id="f4852-112">這個命令會取得訂閱中的所有 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="f4852-112">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="f4852-113">範例2：以特定名稱取得所有 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="f4852-113">Example 2: Get all API Management services by a specific name</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="f4852-114">這個命令會透過名稱取得所有 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="f4852-114">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="f4852-115">參數</span><span class="sxs-lookup"><span data-stu-id="f4852-115">PARAMETERS</span></span>

### <span data-ttu-id="f4852-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4852-116">-DefaultProfile</span></span>
<span data-ttu-id="f4852-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4852-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="f4852-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="f4852-118">-Name</span></span>
<span data-ttu-id="f4852-119">指定 API 管理服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4852-119">Specifies the name of API Management service.</span></span>

```yaml
Type: String
Parameter Sets: GetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4852-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4852-120">-ResourceGroupName</span></span>
<span data-ttu-id="f4852-121">指定此 Cmdlet 取得 API 管理服務所依據之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4852-121">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroup, GetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4852-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4852-122">CommonParameters</span></span>
<span data-ttu-id="f4852-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f4852-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4852-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f4852-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4852-125">輸入</span><span class="sxs-lookup"><span data-stu-id="f4852-125">INPUTS</span></span>

### <span data-ttu-id="f4852-126">所有</span><span class="sxs-lookup"><span data-stu-id="f4852-126">None</span></span>
<span data-ttu-id="f4852-127">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="f4852-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f4852-128">輸出</span><span class="sxs-lookup"><span data-stu-id="f4852-128">OUTPUTS</span></span>

### <span data-ttu-id="f4852-129">[System.object]. 清單 ' 1 [ApiManagement]。 PsApiManagement]</span><span class="sxs-lookup"><span data-stu-id="f4852-129">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement]</span></span>

## <span data-ttu-id="f4852-130">筆記</span><span class="sxs-lookup"><span data-stu-id="f4852-130">NOTES</span></span>

## <span data-ttu-id="f4852-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4852-131">RELATED LINKS</span></span>

[<span data-ttu-id="f4852-132">備份-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="f4852-132">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="f4852-133">新-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="f4852-133">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="f4852-134">移除-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="f4852-134">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="f4852-135">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="f4852-135">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


