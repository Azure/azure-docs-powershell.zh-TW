---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
ms.openlocfilehash: b2c623d46dcc2d84e2c90ae5f3d94cfb54f7224a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450135"
---
# <span data-ttu-id="e4902-101">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="e4902-101">Get-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="e4902-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e4902-102">SYNOPSIS</span></span>
<span data-ttu-id="e4902-103">取得清單或指定的 API 操作。</span><span class="sxs-lookup"><span data-stu-id="e4902-103">Gets a list or a specified API Operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4902-104">句法</span><span class="sxs-lookup"><span data-stu-id="e4902-104">SYNTAX</span></span>

### <span data-ttu-id="e4902-105">所有 API 作業 (預設) </span><span class="sxs-lookup"><span data-stu-id="e4902-105">All API Operations (Default)</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4902-106">依識別碼尋找</span><span class="sxs-lookup"><span data-stu-id="e4902-106">Find by ID</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4902-107">說明</span><span class="sxs-lookup"><span data-stu-id="e4902-107">DESCRIPTION</span></span>
<span data-ttu-id="e4902-108">**AzureRmApiManagementOperation** 會取得清單或指定的 API 操作。</span><span class="sxs-lookup"><span data-stu-id="e4902-108">The **Get-AzureRmApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="e4902-109">示例</span><span class="sxs-lookup"><span data-stu-id="e4902-109">EXAMPLES</span></span>

### <span data-ttu-id="e4902-110">範例1：取得所有 API 管理作業</span><span class="sxs-lookup"><span data-stu-id="e4902-110">Example 1: Get all API management operations</span></span>
```
PS C:\>Get-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId
```

<span data-ttu-id="e4902-111">這個命令會取得所有 API 管理作業。</span><span class="sxs-lookup"><span data-stu-id="e4902-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="e4902-112">範例2：依作業 ID 取得 API 管理作業</span><span class="sxs-lookup"><span data-stu-id="e4902-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>Get-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="e4902-113">這個命令會透過名為 Operation0003 的操作 ID 取得 API 管理作業。</span><span class="sxs-lookup"><span data-stu-id="e4902-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="e4902-114">參數</span><span class="sxs-lookup"><span data-stu-id="e4902-114">PARAMETERS</span></span>

### <span data-ttu-id="e4902-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e4902-115">-ApiId</span></span>
<span data-ttu-id="e4902-116">指定 API 操作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e4902-116">Specifies the identifier of the API Operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4902-117">-內容</span><span class="sxs-lookup"><span data-stu-id="e4902-117">-Context</span></span>
<span data-ttu-id="e4902-118">指定 **PsApiManagementCoNtext** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="e4902-118">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e4902-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="e4902-119">-OperationId</span></span>
<span data-ttu-id="e4902-120">指定操作識別碼。</span><span class="sxs-lookup"><span data-stu-id="e4902-120">Specifies the operation identifier.</span></span>

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

### <span data-ttu-id="e4902-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4902-121">-DefaultProfile</span></span>
<span data-ttu-id="e4902-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e4902-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4902-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4902-123">CommonParameters</span></span>
<span data-ttu-id="e4902-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e4902-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4902-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e4902-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4902-126">輸入</span><span class="sxs-lookup"><span data-stu-id="e4902-126">INPUTS</span></span>

## <span data-ttu-id="e4902-127">輸出</span><span class="sxs-lookup"><span data-stu-id="e4902-127">OUTPUTS</span></span>

### <span data-ttu-id="e4902-128">IList<ApiManagement. ServiceManagement. PsApiManagementOperation]></span><span class="sxs-lookup"><span data-stu-id="e4902-128">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation></span></span>

## <span data-ttu-id="e4902-129">筆記</span><span class="sxs-lookup"><span data-stu-id="e4902-129">NOTES</span></span>

## <span data-ttu-id="e4902-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="e4902-130">RELATED LINKS</span></span>

[<span data-ttu-id="e4902-131">新-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="e4902-131">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="e4902-132">移除-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="e4902-132">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="e4902-133">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="e4902-133">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


