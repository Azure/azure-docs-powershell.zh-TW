---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
ms.openlocfilehash: 014ff118fd1a696eadfcece23c8b0fb8090fda39
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614061"
---
# <span data-ttu-id="e490f-101">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e490f-101">Get-AzApiManagementBackend</span></span>

## <span data-ttu-id="e490f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e490f-102">SYNOPSIS</span></span>
<span data-ttu-id="e490f-103">取得後端的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e490f-103">Get the details of the Backend.</span></span>

## <span data-ttu-id="e490f-104">句法</span><span class="sxs-lookup"><span data-stu-id="e490f-104">SYNTAX</span></span>

### <span data-ttu-id="e490f-105">CoNtextParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e490f-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e490f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e490f-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementBackend [-BackendId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e490f-107">說明</span><span class="sxs-lookup"><span data-stu-id="e490f-107">DESCRIPTION</span></span>
<span data-ttu-id="e490f-108">取得後端的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e490f-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="e490f-109">示例</span><span class="sxs-lookup"><span data-stu-id="e490f-109">EXAMPLES</span></span>

### <span data-ttu-id="e490f-110">範例1：取得所有 Backends</span><span class="sxs-lookup"><span data-stu-id="e490f-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext
```

<span data-ttu-id="e490f-111">取得 Api 管理服務中設定的所有 Backends 的清單。</span><span class="sxs-lookup"><span data-stu-id="e490f-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="e490f-112">範例2：取得識別碼123指定的後端</span><span class="sxs-lookup"><span data-stu-id="e490f-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="e490f-113">取得識別碼「123」所識別之指定後端的詳細資料</span><span class="sxs-lookup"><span data-stu-id="e490f-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="e490f-114">參數</span><span class="sxs-lookup"><span data-stu-id="e490f-114">PARAMETERS</span></span>

### <span data-ttu-id="e490f-115">-BackendId</span><span class="sxs-lookup"><span data-stu-id="e490f-115">-BackendId</span></span>
<span data-ttu-id="e490f-116">後端的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e490f-116">Identifier of a backend.</span></span>
<span data-ttu-id="e490f-117">如果已指定，將會嘗試透過識別碼尋找後端。</span><span class="sxs-lookup"><span data-stu-id="e490f-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="e490f-118">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="e490f-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="e490f-119">-內容</span><span class="sxs-lookup"><span data-stu-id="e490f-119">-Context</span></span>
<span data-ttu-id="e490f-120">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="e490f-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e490f-121">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="e490f-121">This parameter is required.</span></span>

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

### <span data-ttu-id="e490f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e490f-122">-DefaultProfile</span></span>
<span data-ttu-id="e490f-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e490f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e490f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e490f-124">-ResourceId</span></span>
<span data-ttu-id="e490f-125">後端的 Arm 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e490f-125">Arm Resource Identifier of the backend.</span></span> <span data-ttu-id="e490f-126">如果已指定，將會嘗試透過識別碼尋找後端。</span><span class="sxs-lookup"><span data-stu-id="e490f-126">If specified will try to find backend by the identifier.</span></span> <span data-ttu-id="e490f-127">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="e490f-127">This parameter is required.</span></span>

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

### <span data-ttu-id="e490f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e490f-128">CommonParameters</span></span>
<span data-ttu-id="e490f-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e490f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e490f-130">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e490f-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e490f-131">輸入</span><span class="sxs-lookup"><span data-stu-id="e490f-131">INPUTS</span></span>

### <span data-ttu-id="e490f-132">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="e490f-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e490f-133">System.object</span><span class="sxs-lookup"><span data-stu-id="e490f-133">System.String</span></span>

## <span data-ttu-id="e490f-134">輸出</span><span class="sxs-lookup"><span data-stu-id="e490f-134">OUTPUTS</span></span>

### <span data-ttu-id="e490f-135">ServiceManagement. PsApiManagementBackend （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="e490f-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="e490f-136">筆記</span><span class="sxs-lookup"><span data-stu-id="e490f-136">NOTES</span></span>

## <span data-ttu-id="e490f-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="e490f-137">RELATED LINKS</span></span>

[<span data-ttu-id="e490f-138">新-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e490f-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="e490f-139">新-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="e490f-139">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="e490f-140">新-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="e490f-140">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="e490f-141">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e490f-141">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="e490f-142">移除-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e490f-142">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
