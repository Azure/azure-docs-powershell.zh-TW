---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
ms.openlocfilehash: 435e167b713934962daf0cf27fc0d844caee8dcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446575"
---
# <span data-ttu-id="d197d-101">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d197d-101">Get-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="d197d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d197d-102">SYNOPSIS</span></span>
<span data-ttu-id="d197d-103">取得 API。</span><span class="sxs-lookup"><span data-stu-id="d197d-103">Gets an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d197d-104">句法</span><span class="sxs-lookup"><span data-stu-id="d197d-104">SYNTAX</span></span>

### <span data-ttu-id="d197d-105">GetAllApis (預設) </span><span class="sxs-lookup"><span data-stu-id="d197d-105">GetAllApis (Default)</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d197d-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="d197d-106">GetByApiId</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d197d-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="d197d-107">GetByName</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d197d-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="d197d-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d197d-109">說明</span><span class="sxs-lookup"><span data-stu-id="d197d-109">DESCRIPTION</span></span>
<span data-ttu-id="d197d-110">**AzureRmApiManagementApi** Cmdlet 會取得一或多個 Azure API 管理 api。</span><span class="sxs-lookup"><span data-stu-id="d197d-110">The **Get-AzureRmApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="d197d-111">示例</span><span class="sxs-lookup"><span data-stu-id="d197d-111">EXAMPLES</span></span>

### <span data-ttu-id="d197d-112">範例1：取得所有管理 Api</span><span class="sxs-lookup"><span data-stu-id="d197d-112">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="d197d-113">這個命令會取得指定內容的所有 Api。</span><span class="sxs-lookup"><span data-stu-id="d197d-113">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="d197d-114">範例2：依識別碼取得管理 API</span><span class="sxs-lookup"><span data-stu-id="d197d-114">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="d197d-115">這個命令會取得具有指定識別碼的 API。</span><span class="sxs-lookup"><span data-stu-id="d197d-115">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="d197d-116">範例3：依名稱取得管理 API</span><span class="sxs-lookup"><span data-stu-id="d197d-116">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="d197d-117">這個命令會取得具有指定名稱的 API。</span><span class="sxs-lookup"><span data-stu-id="d197d-117">This command gets the API with the specified name.</span></span>

## <span data-ttu-id="d197d-118">參數</span><span class="sxs-lookup"><span data-stu-id="d197d-118">PARAMETERS</span></span>

### <span data-ttu-id="d197d-119">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d197d-119">-ApiId</span></span>
<span data-ttu-id="d197d-120">指定要取得的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="d197d-120">Specifies the ID of the API to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByApiId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d197d-121">-內容</span><span class="sxs-lookup"><span data-stu-id="d197d-121">-Context</span></span>
<span data-ttu-id="d197d-122">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="d197d-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d197d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d197d-123">-DefaultProfile</span></span>
<span data-ttu-id="d197d-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d197d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="d197d-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="d197d-125">-Name</span></span>
<span data-ttu-id="d197d-126">指定要取得的 API 名稱。</span><span class="sxs-lookup"><span data-stu-id="d197d-126">Specifies the name of the API to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d197d-127">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="d197d-127">-ProductId</span></span>
<span data-ttu-id="d197d-128">指定要取得 API 的產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="d197d-128">Specifies the ID of the product for which to get the API.</span></span>

```yaml
Type: String
Parameter Sets: GetByProductId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d197d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d197d-129">CommonParameters</span></span>
<span data-ttu-id="d197d-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d197d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d197d-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d197d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d197d-132">輸入</span><span class="sxs-lookup"><span data-stu-id="d197d-132">INPUTS</span></span>

### <span data-ttu-id="d197d-133">所有</span><span class="sxs-lookup"><span data-stu-id="d197d-133">None</span></span>
<span data-ttu-id="d197d-134">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="d197d-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d197d-135">輸出</span><span class="sxs-lookup"><span data-stu-id="d197d-135">OUTPUTS</span></span>

### <span data-ttu-id="d197d-136">ServiceManagement. PsApiManagementApi （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="d197d-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="d197d-137">指定 ApiManagement 服務中 Api 的詳細資料</span><span class="sxs-lookup"><span data-stu-id="d197d-137">The details of the Api in a given ApiManagement service</span></span>

### <span data-ttu-id="d197d-138">IList<ApiManagement. ServiceManagement. PsApiManagementApi]></span><span class="sxs-lookup"><span data-stu-id="d197d-138">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi></span></span>
<span data-ttu-id="d197d-139">指定 ApiManagement 服務中的 Api 清單</span><span class="sxs-lookup"><span data-stu-id="d197d-139">The list of Apis in a given ApiManagement service</span></span>

## <span data-ttu-id="d197d-140">筆記</span><span class="sxs-lookup"><span data-stu-id="d197d-140">NOTES</span></span>

## <span data-ttu-id="d197d-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="d197d-141">RELATED LINKS</span></span>

[<span data-ttu-id="d197d-142">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d197d-142">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="d197d-143">匯入-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d197d-143">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="d197d-144">新-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d197d-144">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="d197d-145">移除-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d197d-145">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="d197d-146">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d197d-146">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


