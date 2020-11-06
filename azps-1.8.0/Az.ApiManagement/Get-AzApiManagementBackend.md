---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
ms.openlocfilehash: 88a48edf3ae7e576aa78e989a5fda7515499a7f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611629"
---
# <span data-ttu-id="48e61-101">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="48e61-101">Get-AzApiManagementBackend</span></span>

## <span data-ttu-id="48e61-102">摘要</span><span class="sxs-lookup"><span data-stu-id="48e61-102">SYNOPSIS</span></span>
<span data-ttu-id="48e61-103">取得後端的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="48e61-103">Get the details of the Backend.</span></span>

## <span data-ttu-id="48e61-104">句法</span><span class="sxs-lookup"><span data-stu-id="48e61-104">SYNTAX</span></span>

### <span data-ttu-id="48e61-105">GetAllBackends (預設) </span><span class="sxs-lookup"><span data-stu-id="48e61-105">GetAllBackends (Default)</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="48e61-106">GetByBackendId</span><span class="sxs-lookup"><span data-stu-id="48e61-106">GetByBackendId</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48e61-107">說明</span><span class="sxs-lookup"><span data-stu-id="48e61-107">DESCRIPTION</span></span>
<span data-ttu-id="48e61-108">取得後端的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="48e61-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="48e61-109">示例</span><span class="sxs-lookup"><span data-stu-id="48e61-109">EXAMPLES</span></span>

### <span data-ttu-id="48e61-110">範例1：取得所有 Backends</span><span class="sxs-lookup"><span data-stu-id="48e61-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext
```

<span data-ttu-id="48e61-111">取得 Api 管理服務中設定的所有 Backends 的清單。</span><span class="sxs-lookup"><span data-stu-id="48e61-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="48e61-112">範例2：取得識別碼123指定的後端</span><span class="sxs-lookup"><span data-stu-id="48e61-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="48e61-113">取得識別碼「123」所識別之指定後端的詳細資料</span><span class="sxs-lookup"><span data-stu-id="48e61-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="48e61-114">參數</span><span class="sxs-lookup"><span data-stu-id="48e61-114">PARAMETERS</span></span>

### <span data-ttu-id="48e61-115">-BackendId</span><span class="sxs-lookup"><span data-stu-id="48e61-115">-BackendId</span></span>
<span data-ttu-id="48e61-116">後端的識別碼。</span><span class="sxs-lookup"><span data-stu-id="48e61-116">Identifier of a backend.</span></span>
<span data-ttu-id="48e61-117">如果已指定，將會嘗試透過識別碼尋找後端。</span><span class="sxs-lookup"><span data-stu-id="48e61-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="48e61-118">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="48e61-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="48e61-119">-內容</span><span class="sxs-lookup"><span data-stu-id="48e61-119">-Context</span></span>
<span data-ttu-id="48e61-120">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="48e61-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="48e61-121">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="48e61-121">This parameter is required.</span></span>

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

### <span data-ttu-id="48e61-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48e61-122">-DefaultProfile</span></span>
<span data-ttu-id="48e61-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="48e61-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e61-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48e61-124">CommonParameters</span></span>
<span data-ttu-id="48e61-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="48e61-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48e61-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="48e61-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48e61-127">輸入</span><span class="sxs-lookup"><span data-stu-id="48e61-127">INPUTS</span></span>

### <span data-ttu-id="48e61-128">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="48e61-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="48e61-129">System.object</span><span class="sxs-lookup"><span data-stu-id="48e61-129">System.String</span></span>

## <span data-ttu-id="48e61-130">輸出</span><span class="sxs-lookup"><span data-stu-id="48e61-130">OUTPUTS</span></span>

### <span data-ttu-id="48e61-131">ServiceManagement. PsApiManagementBackend （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="48e61-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="48e61-132">筆記</span><span class="sxs-lookup"><span data-stu-id="48e61-132">NOTES</span></span>

## <span data-ttu-id="48e61-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="48e61-133">RELATED LINKS</span></span>

[<span data-ttu-id="48e61-134">新-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="48e61-134">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="48e61-135">新-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="48e61-135">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="48e61-136">新-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="48e61-136">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="48e61-137">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="48e61-137">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="48e61-138">移除-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="48e61-138">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
