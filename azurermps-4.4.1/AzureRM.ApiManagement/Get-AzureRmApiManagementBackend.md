---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
ms.openlocfilehash: 4f54b361482bad24826d7120e53f96ce8d3b9eef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450940"
---
# <span data-ttu-id="69dd5-101">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="69dd5-101">Get-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="69dd5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="69dd5-102">SYNOPSIS</span></span>
<span data-ttu-id="69dd5-103">取得後端的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="69dd5-103">Get the details of the Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69dd5-104">句法</span><span class="sxs-lookup"><span data-stu-id="69dd5-104">SYNTAX</span></span>

### <span data-ttu-id="69dd5-105">取得所有 backends (預設) </span><span class="sxs-lookup"><span data-stu-id="69dd5-105">Get all backends (Default)</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="69dd5-106">依後端識別碼取得</span><span class="sxs-lookup"><span data-stu-id="69dd5-106">Get by backend ID</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69dd5-107">說明</span><span class="sxs-lookup"><span data-stu-id="69dd5-107">DESCRIPTION</span></span>
<span data-ttu-id="69dd5-108">取得後端的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="69dd5-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="69dd5-109">示例</span><span class="sxs-lookup"><span data-stu-id="69dd5-109">EXAMPLES</span></span>

### <span data-ttu-id="69dd5-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="69dd5-110">--------------------------  Example 1  --------------------------</span></span>
<span data-ttu-id="69dd5-111">@ {段落 = PS C： \\ \> }</span><span class="sxs-lookup"><span data-stu-id="69dd5-111">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementBackend -Context $apimContext
```

<span data-ttu-id="69dd5-112">取得 Api 管理服務中設定的所有 Backends 的清單。</span><span class="sxs-lookup"><span data-stu-id="69dd5-112">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="69dd5-113">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="69dd5-113">--------------------------  Example 2  --------------------------</span></span>
<span data-ttu-id="69dd5-114">@ {段落 = PS C： \\ \> }</span><span class="sxs-lookup"><span data-stu-id="69dd5-114">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="69dd5-115">取得識別碼「123」所識別之指定後端的詳細資料</span><span class="sxs-lookup"><span data-stu-id="69dd5-115">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="69dd5-116">參數</span><span class="sxs-lookup"><span data-stu-id="69dd5-116">PARAMETERS</span></span>

### <span data-ttu-id="69dd5-117">-BackendId</span><span class="sxs-lookup"><span data-stu-id="69dd5-117">-BackendId</span></span>
<span data-ttu-id="69dd5-118">後端的識別碼。</span><span class="sxs-lookup"><span data-stu-id="69dd5-118">Identifier of a backend.</span></span>
<span data-ttu-id="69dd5-119">如果已指定，將會嘗試透過識別碼尋找後端。</span><span class="sxs-lookup"><span data-stu-id="69dd5-119">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="69dd5-120">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="69dd5-120">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by backend ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69dd5-121">-內容</span><span class="sxs-lookup"><span data-stu-id="69dd5-121">-Context</span></span>
<span data-ttu-id="69dd5-122">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="69dd5-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="69dd5-123">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="69dd5-123">This parameter is required.</span></span>

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

### <span data-ttu-id="69dd5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69dd5-124">-DefaultProfile</span></span>
<span data-ttu-id="69dd5-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="69dd5-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69dd5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69dd5-126">CommonParameters</span></span>
<span data-ttu-id="69dd5-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="69dd5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69dd5-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="69dd5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69dd5-129">輸入</span><span class="sxs-lookup"><span data-stu-id="69dd5-129">INPUTS</span></span>

## <span data-ttu-id="69dd5-130">輸出</span><span class="sxs-lookup"><span data-stu-id="69dd5-130">OUTPUTS</span></span>

### <span data-ttu-id="69dd5-131">IList<ApiManagement. ServiceManagement. PsApiManagementBackend]></span><span class="sxs-lookup"><span data-stu-id="69dd5-131">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend></span></span>

### <span data-ttu-id="69dd5-132">PsApiManagementLogger.. PsApiManagementBackend （ApiManagement） ServiceManagement</span><span class="sxs-lookup"><span data-stu-id="69dd5-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger.PsApiManagementBackend</span></span>

## <span data-ttu-id="69dd5-133">筆記</span><span class="sxs-lookup"><span data-stu-id="69dd5-133">NOTES</span></span>

## <span data-ttu-id="69dd5-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="69dd5-134">RELATED LINKS</span></span>

[<span data-ttu-id="69dd5-135">新-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="69dd5-135">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="69dd5-136">新-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="69dd5-136">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="69dd5-137">新-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="69dd5-137">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="69dd5-138">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="69dd5-138">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="69dd5-139">移除-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="69dd5-139">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
