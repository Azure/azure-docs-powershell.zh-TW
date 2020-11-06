---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
ms.openlocfilehash: 11d832bc74aca4ac274ee17ff0b38de06b77e377
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447537"
---
# <span data-ttu-id="419ad-101">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="419ad-101">Get-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="419ad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="419ad-102">SYNOPSIS</span></span>
<span data-ttu-id="419ad-103">取得後端的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="419ad-103">Get the details of the Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="419ad-104">句法</span><span class="sxs-lookup"><span data-stu-id="419ad-104">SYNTAX</span></span>

### <span data-ttu-id="419ad-105">GetAllBackends (預設) </span><span class="sxs-lookup"><span data-stu-id="419ad-105">GetAllBackends (Default)</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="419ad-106">GetByBackendId</span><span class="sxs-lookup"><span data-stu-id="419ad-106">GetByBackendId</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="419ad-107">說明</span><span class="sxs-lookup"><span data-stu-id="419ad-107">DESCRIPTION</span></span>
<span data-ttu-id="419ad-108">取得後端的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="419ad-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="419ad-109">示例</span><span class="sxs-lookup"><span data-stu-id="419ad-109">EXAMPLES</span></span>

### <span data-ttu-id="419ad-110">範例1：取得所有 Backends</span><span class="sxs-lookup"><span data-stu-id="419ad-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementBackend -Context $apimContext
```

<span data-ttu-id="419ad-111">取得 Api 管理服務中設定的所有 Backends 的清單。</span><span class="sxs-lookup"><span data-stu-id="419ad-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="419ad-112">範例2：取得識別碼123指定的後端</span><span class="sxs-lookup"><span data-stu-id="419ad-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="419ad-113">取得識別碼「123」所識別之指定後端的詳細資料</span><span class="sxs-lookup"><span data-stu-id="419ad-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="419ad-114">參數</span><span class="sxs-lookup"><span data-stu-id="419ad-114">PARAMETERS</span></span>

### <span data-ttu-id="419ad-115">-BackendId</span><span class="sxs-lookup"><span data-stu-id="419ad-115">-BackendId</span></span>
<span data-ttu-id="419ad-116">後端的識別碼。</span><span class="sxs-lookup"><span data-stu-id="419ad-116">Identifier of a backend.</span></span>
<span data-ttu-id="419ad-117">如果已指定，將會嘗試透過識別碼尋找後端。</span><span class="sxs-lookup"><span data-stu-id="419ad-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="419ad-118">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="419ad-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByBackendId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="419ad-119">-內容</span><span class="sxs-lookup"><span data-stu-id="419ad-119">-Context</span></span>
<span data-ttu-id="419ad-120">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="419ad-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="419ad-121">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="419ad-121">This parameter is required.</span></span>

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

### <span data-ttu-id="419ad-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="419ad-122">-DefaultProfile</span></span>
<span data-ttu-id="419ad-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="419ad-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="419ad-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="419ad-124">CommonParameters</span></span>
<span data-ttu-id="419ad-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="419ad-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="419ad-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="419ad-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="419ad-127">輸入</span><span class="sxs-lookup"><span data-stu-id="419ad-127">INPUTS</span></span>

### <span data-ttu-id="419ad-128">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="419ad-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="419ad-129">System.object</span><span class="sxs-lookup"><span data-stu-id="419ad-129">System.String</span></span>

## <span data-ttu-id="419ad-130">輸出</span><span class="sxs-lookup"><span data-stu-id="419ad-130">OUTPUTS</span></span>

### <span data-ttu-id="419ad-131">ServiceManagement. PsApiManagementBackend （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="419ad-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="419ad-132">筆記</span><span class="sxs-lookup"><span data-stu-id="419ad-132">NOTES</span></span>

## <span data-ttu-id="419ad-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="419ad-133">RELATED LINKS</span></span>

[<span data-ttu-id="419ad-134">新-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="419ad-134">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="419ad-135">新-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="419ad-135">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="419ad-136">新-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="419ad-136">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="419ad-137">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="419ad-137">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="419ad-138">移除-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="419ad-138">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
