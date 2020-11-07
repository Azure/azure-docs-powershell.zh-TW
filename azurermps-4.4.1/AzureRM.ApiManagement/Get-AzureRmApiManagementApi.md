---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
ms.openlocfilehash: 95784b084f6d106413c65b840dd73f313a47799e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625733"
---
# <span data-ttu-id="7b8fb-101">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7b8fb-101">Get-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="7b8fb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7b8fb-102">SYNOPSIS</span></span>
<span data-ttu-id="7b8fb-103">取得 API。</span><span class="sxs-lookup"><span data-stu-id="7b8fb-103">Gets an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b8fb-104">句法</span><span class="sxs-lookup"><span data-stu-id="7b8fb-104">SYNTAX</span></span>

### <span data-ttu-id="7b8fb-105">所有 Api (預設) </span><span class="sxs-lookup"><span data-stu-id="7b8fb-105">All APIs (Default)</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b8fb-106">依識別碼尋找</span><span class="sxs-lookup"><span data-stu-id="7b8fb-106">Find by ID</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b8fb-107">依名稱尋找</span><span class="sxs-lookup"><span data-stu-id="7b8fb-107">Find by Name</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b8fb-108">依產品識別碼尋找</span><span class="sxs-lookup"><span data-stu-id="7b8fb-108">Find by product ID</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b8fb-109">說明</span><span class="sxs-lookup"><span data-stu-id="7b8fb-109">DESCRIPTION</span></span>
<span data-ttu-id="7b8fb-110">**AzureRmApiManagementApi** Cmdlet 會取得一或多個 Azure API 管理 api。</span><span class="sxs-lookup"><span data-stu-id="7b8fb-110">The **Get-AzureRmApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="7b8fb-111">示例</span><span class="sxs-lookup"><span data-stu-id="7b8fb-111">EXAMPLES</span></span>

### <span data-ttu-id="7b8fb-112">範例1：取得所有管理 Api</span><span class="sxs-lookup"><span data-stu-id="7b8fb-112">Example 1: Get all management APIs</span></span>
```
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="7b8fb-113">這個命令會取得指定內容的所有 Api。</span><span class="sxs-lookup"><span data-stu-id="7b8fb-113">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="7b8fb-114">範例2：依識別碼取得管理 API</span><span class="sxs-lookup"><span data-stu-id="7b8fb-114">Example 2: Get a management API by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="7b8fb-115">這個命令會取得具有指定識別碼的 API。</span><span class="sxs-lookup"><span data-stu-id="7b8fb-115">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="7b8fb-116">範例3：依名稱取得管理 API</span><span class="sxs-lookup"><span data-stu-id="7b8fb-116">Example 3: Get a management API by name</span></span>
```
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="7b8fb-117">這個命令會取得具有指定名稱的 API。</span><span class="sxs-lookup"><span data-stu-id="7b8fb-117">This command gets the API with the specified name.</span></span>

## <span data-ttu-id="7b8fb-118">參數</span><span class="sxs-lookup"><span data-stu-id="7b8fb-118">PARAMETERS</span></span>

### <span data-ttu-id="7b8fb-119">-ApiId</span><span class="sxs-lookup"><span data-stu-id="7b8fb-119">-ApiId</span></span>
<span data-ttu-id="7b8fb-120">指定要取得的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="7b8fb-120">Specifies the ID of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b8fb-121">-內容</span><span class="sxs-lookup"><span data-stu-id="7b8fb-121">-Context</span></span>
<span data-ttu-id="7b8fb-122">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="7b8fb-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b8fb-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="7b8fb-123">-Name</span></span>
<span data-ttu-id="7b8fb-124">指定要取得的 API 名稱。</span><span class="sxs-lookup"><span data-stu-id="7b8fb-124">Specifies the name of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by Name
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b8fb-125">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="7b8fb-125">-ProductId</span></span>
<span data-ttu-id="7b8fb-126">指定要取得 API 的產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="7b8fb-126">Specifies the ID of the product for which to get the API.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by product ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b8fb-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b8fb-127">-DefaultProfile</span></span>
<span data-ttu-id="7b8fb-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7b8fb-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b8fb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b8fb-129">CommonParameters</span></span>
<span data-ttu-id="7b8fb-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7b8fb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b8fb-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7b8fb-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b8fb-132">輸入</span><span class="sxs-lookup"><span data-stu-id="7b8fb-132">INPUTS</span></span>

## <span data-ttu-id="7b8fb-133">輸出</span><span class="sxs-lookup"><span data-stu-id="7b8fb-133">OUTPUTS</span></span>

### <span data-ttu-id="7b8fb-134">IList<ApiManagement. ServiceManagement. PsApiManagementApi]></span><span class="sxs-lookup"><span data-stu-id="7b8fb-134">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi></span></span>

## <span data-ttu-id="7b8fb-135">筆記</span><span class="sxs-lookup"><span data-stu-id="7b8fb-135">NOTES</span></span>

## <span data-ttu-id="7b8fb-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="7b8fb-136">RELATED LINKS</span></span>

[<span data-ttu-id="7b8fb-137">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7b8fb-137">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="7b8fb-138">匯入-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7b8fb-138">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="7b8fb-139">新-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7b8fb-139">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="7b8fb-140">移除-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7b8fb-140">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="7b8fb-141">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7b8fb-141">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


