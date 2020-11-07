---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
ms.openlocfilehash: 4781800ea9a6f8526ddee5e06b90b73ea676bf88
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957885"
---
# <span data-ttu-id="ec79d-101">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ec79d-101">Get-AzApiManagementBackend</span></span>

## <span data-ttu-id="ec79d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ec79d-102">SYNOPSIS</span></span>
<span data-ttu-id="ec79d-103">取得後端的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ec79d-103">Get the details of the Backend.</span></span>

## <span data-ttu-id="ec79d-104">句法</span><span class="sxs-lookup"><span data-stu-id="ec79d-104">SYNTAX</span></span>

### <span data-ttu-id="ec79d-105">CoNtextParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ec79d-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec79d-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec79d-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementBackend [-BackendId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec79d-107">說明</span><span class="sxs-lookup"><span data-stu-id="ec79d-107">DESCRIPTION</span></span>
<span data-ttu-id="ec79d-108">取得後端的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ec79d-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="ec79d-109">示例</span><span class="sxs-lookup"><span data-stu-id="ec79d-109">EXAMPLES</span></span>

### <span data-ttu-id="ec79d-110">範例1：取得所有 Backends</span><span class="sxs-lookup"><span data-stu-id="ec79d-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext
```

<span data-ttu-id="ec79d-111">取得 Api 管理服務中設定的所有 Backends 的清單。</span><span class="sxs-lookup"><span data-stu-id="ec79d-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="ec79d-112">範例2：取得識別碼123指定的後端</span><span class="sxs-lookup"><span data-stu-id="ec79d-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="ec79d-113">取得識別碼「123」所識別之指定後端的詳細資料</span><span class="sxs-lookup"><span data-stu-id="ec79d-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="ec79d-114">參數</span><span class="sxs-lookup"><span data-stu-id="ec79d-114">PARAMETERS</span></span>

### <span data-ttu-id="ec79d-115">-BackendId</span><span class="sxs-lookup"><span data-stu-id="ec79d-115">-BackendId</span></span>
<span data-ttu-id="ec79d-116">後端的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ec79d-116">Identifier of a backend.</span></span>
<span data-ttu-id="ec79d-117">如果已指定，將會嘗試透過識別碼尋找後端。</span><span class="sxs-lookup"><span data-stu-id="ec79d-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="ec79d-118">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="ec79d-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="ec79d-119">-內容</span><span class="sxs-lookup"><span data-stu-id="ec79d-119">-Context</span></span>
<span data-ttu-id="ec79d-120">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="ec79d-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ec79d-121">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="ec79d-121">This parameter is required.</span></span>

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

### <span data-ttu-id="ec79d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec79d-122">-DefaultProfile</span></span>
<span data-ttu-id="ec79d-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ec79d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec79d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec79d-124">-ResourceId</span></span>
<span data-ttu-id="ec79d-125">後端的 Arm 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ec79d-125">Arm Resource Identifier of the backend.</span></span> <span data-ttu-id="ec79d-126">如果已指定，將會嘗試透過識別碼尋找後端。</span><span class="sxs-lookup"><span data-stu-id="ec79d-126">If specified will try to find backend by the identifier.</span></span> <span data-ttu-id="ec79d-127">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="ec79d-127">This parameter is required.</span></span>

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

### <span data-ttu-id="ec79d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec79d-128">CommonParameters</span></span>
<span data-ttu-id="ec79d-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ec79d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec79d-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ec79d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec79d-131">輸入</span><span class="sxs-lookup"><span data-stu-id="ec79d-131">INPUTS</span></span>

### <span data-ttu-id="ec79d-132">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="ec79d-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ec79d-133">System.object</span><span class="sxs-lookup"><span data-stu-id="ec79d-133">System.String</span></span>

## <span data-ttu-id="ec79d-134">輸出</span><span class="sxs-lookup"><span data-stu-id="ec79d-134">OUTPUTS</span></span>

### <span data-ttu-id="ec79d-135">ServiceManagement. PsApiManagementBackend （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="ec79d-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="ec79d-136">筆記</span><span class="sxs-lookup"><span data-stu-id="ec79d-136">NOTES</span></span>

## <span data-ttu-id="ec79d-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec79d-137">RELATED LINKS</span></span>

[<span data-ttu-id="ec79d-138">新-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ec79d-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="ec79d-139">新-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="ec79d-139">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="ec79d-140">新-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="ec79d-140">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="ec79d-141">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ec79d-141">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="ec79d-142">移除-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ec79d-142">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
