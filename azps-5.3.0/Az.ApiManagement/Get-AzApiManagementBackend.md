---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
ms.openlocfilehash: 4781800ea9a6f8526ddee5e06b90b73ea676bf88
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447623"
---
# <span data-ttu-id="7b00c-101">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7b00c-101">Get-AzApiManagementBackend</span></span>

## <span data-ttu-id="7b00c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7b00c-102">SYNOPSIS</span></span>
<span data-ttu-id="7b00c-103">取得後端的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7b00c-103">Get the details of the Backend.</span></span>

## <span data-ttu-id="7b00c-104">句法</span><span class="sxs-lookup"><span data-stu-id="7b00c-104">SYNTAX</span></span>

### <span data-ttu-id="7b00c-105">CoNtextParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7b00c-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b00c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b00c-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementBackend [-BackendId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b00c-107">說明</span><span class="sxs-lookup"><span data-stu-id="7b00c-107">DESCRIPTION</span></span>
<span data-ttu-id="7b00c-108">取得後端的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7b00c-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="7b00c-109">示例</span><span class="sxs-lookup"><span data-stu-id="7b00c-109">EXAMPLES</span></span>

### <span data-ttu-id="7b00c-110">範例1：取得所有 Backends</span><span class="sxs-lookup"><span data-stu-id="7b00c-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext
```

<span data-ttu-id="7b00c-111">取得 Api 管理服務中設定的所有 Backends 的清單。</span><span class="sxs-lookup"><span data-stu-id="7b00c-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="7b00c-112">範例2：取得識別碼123指定的後端</span><span class="sxs-lookup"><span data-stu-id="7b00c-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="7b00c-113">取得識別碼「123」所識別之指定後端的詳細資料</span><span class="sxs-lookup"><span data-stu-id="7b00c-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="7b00c-114">參數</span><span class="sxs-lookup"><span data-stu-id="7b00c-114">PARAMETERS</span></span>

### <span data-ttu-id="7b00c-115">-BackendId</span><span class="sxs-lookup"><span data-stu-id="7b00c-115">-BackendId</span></span>
<span data-ttu-id="7b00c-116">後端的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7b00c-116">Identifier of a backend.</span></span>
<span data-ttu-id="7b00c-117">如果已指定，將會嘗試透過識別碼尋找後端。</span><span class="sxs-lookup"><span data-stu-id="7b00c-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="7b00c-118">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="7b00c-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="7b00c-119">-內容</span><span class="sxs-lookup"><span data-stu-id="7b00c-119">-Context</span></span>
<span data-ttu-id="7b00c-120">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="7b00c-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7b00c-121">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="7b00c-121">This parameter is required.</span></span>

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

### <span data-ttu-id="7b00c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b00c-122">-DefaultProfile</span></span>
<span data-ttu-id="7b00c-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7b00c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b00c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b00c-124">-ResourceId</span></span>
<span data-ttu-id="7b00c-125">後端的 Arm 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7b00c-125">Arm Resource Identifier of the backend.</span></span> <span data-ttu-id="7b00c-126">如果已指定，將會嘗試透過識別碼尋找後端。</span><span class="sxs-lookup"><span data-stu-id="7b00c-126">If specified will try to find backend by the identifier.</span></span> <span data-ttu-id="7b00c-127">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="7b00c-127">This parameter is required.</span></span>

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

### <span data-ttu-id="7b00c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b00c-128">CommonParameters</span></span>
<span data-ttu-id="7b00c-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7b00c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b00c-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7b00c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b00c-131">輸入</span><span class="sxs-lookup"><span data-stu-id="7b00c-131">INPUTS</span></span>

### <span data-ttu-id="7b00c-132">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="7b00c-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7b00c-133">System.object</span><span class="sxs-lookup"><span data-stu-id="7b00c-133">System.String</span></span>

## <span data-ttu-id="7b00c-134">輸出</span><span class="sxs-lookup"><span data-stu-id="7b00c-134">OUTPUTS</span></span>

### <span data-ttu-id="7b00c-135">ServiceManagement. PsApiManagementBackend （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="7b00c-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="7b00c-136">筆記</span><span class="sxs-lookup"><span data-stu-id="7b00c-136">NOTES</span></span>

## <span data-ttu-id="7b00c-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="7b00c-137">RELATED LINKS</span></span>

[<span data-ttu-id="7b00c-138">新-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7b00c-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="7b00c-139">新-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="7b00c-139">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="7b00c-140">新-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="7b00c-140">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="7b00c-141">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7b00c-141">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="7b00c-142">移除-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7b00c-142">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
