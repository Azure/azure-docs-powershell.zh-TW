---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
ms.openlocfilehash: ea9975038f1c738461f8c3bbda4cba70bafe8ad9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903049"
---
# <span data-ttu-id="b060a-101">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b060a-101">Get-AzApiManagementBackend</span></span>

## <span data-ttu-id="b060a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b060a-102">SYNOPSIS</span></span>
<span data-ttu-id="b060a-103">取得後端的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="b060a-103">Get the details of the Backend.</span></span>

## <span data-ttu-id="b060a-104">語法</span><span class="sxs-lookup"><span data-stu-id="b060a-104">SYNTAX</span></span>

### <span data-ttu-id="b060a-105">CoNtextParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b060a-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b060a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b060a-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementBackend [-BackendId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b060a-107">描述</span><span class="sxs-lookup"><span data-stu-id="b060a-107">DESCRIPTION</span></span>
<span data-ttu-id="b060a-108">取得後端的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="b060a-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="b060a-109">例子</span><span class="sxs-lookup"><span data-stu-id="b060a-109">EXAMPLES</span></span>

### <span data-ttu-id="b060a-110">範例 1：取得所有後端</span><span class="sxs-lookup"><span data-stu-id="b060a-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext
```

<span data-ttu-id="b060a-111">在 Api 管理服務中，獲得所有已配置的後端清單。</span><span class="sxs-lookup"><span data-stu-id="b060a-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="b060a-112">範例 2：取得由識別碼 123 指定的後端</span><span class="sxs-lookup"><span data-stu-id="b060a-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="b060a-113">取得識別碼 '123' 所識別之指定後端的詳細資訊</span><span class="sxs-lookup"><span data-stu-id="b060a-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="b060a-114">參數</span><span class="sxs-lookup"><span data-stu-id="b060a-114">PARAMETERS</span></span>

### <span data-ttu-id="b060a-115">-後端Id</span><span class="sxs-lookup"><span data-stu-id="b060a-115">-BackendId</span></span>
<span data-ttu-id="b060a-116">後端的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b060a-116">Identifier of a backend.</span></span>
<span data-ttu-id="b060a-117">如果指定，會嘗試根據識別碼尋找後端。</span><span class="sxs-lookup"><span data-stu-id="b060a-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="b060a-118">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="b060a-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="b060a-119">-內容</span><span class="sxs-lookup"><span data-stu-id="b060a-119">-Context</span></span>
<span data-ttu-id="b060a-120">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="b060a-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b060a-121">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="b060a-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b060a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b060a-122">-DefaultProfile</span></span>
<span data-ttu-id="b060a-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b060a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b060a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b060a-124">-ResourceId</span></span>
<span data-ttu-id="b060a-125">後端的 Arm 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b060a-125">Arm Resource Identifier of the backend.</span></span> <span data-ttu-id="b060a-126">如果指定，會嘗試根據識別碼尋找後端。</span><span class="sxs-lookup"><span data-stu-id="b060a-126">If specified will try to find backend by the identifier.</span></span> <span data-ttu-id="b060a-127">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="b060a-127">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b060a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b060a-128">CommonParameters</span></span>
<span data-ttu-id="b060a-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b060a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b060a-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b060a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b060a-131">輸入</span><span class="sxs-lookup"><span data-stu-id="b060a-131">INPUTS</span></span>

### <span data-ttu-id="b060a-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="b060a-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b060a-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b060a-133">System.String</span></span>

## <span data-ttu-id="b060a-134">輸出</span><span class="sxs-lookup"><span data-stu-id="b060a-134">OUTPUTS</span></span>

### <span data-ttu-id="b060a-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b060a-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="b060a-136">筆記</span><span class="sxs-lookup"><span data-stu-id="b060a-136">NOTES</span></span>

## <span data-ttu-id="b060a-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="b060a-137">RELATED LINKS</span></span>

[<span data-ttu-id="b060a-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b060a-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="b060a-139">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="b060a-139">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="b060a-140">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="b060a-140">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="b060a-141">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b060a-141">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="b060a-142">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b060a-142">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
