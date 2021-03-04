---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
ms.openlocfilehash: b7124b00452637ca3e496a0417745ee7719278e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908325"
---
# <span data-ttu-id="46bee-101">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="46bee-101">New-AzApiManagementContext</span></span>

## <span data-ttu-id="46bee-102">簡介</span><span class="sxs-lookup"><span data-stu-id="46bee-102">SYNOPSIS</span></span>
<span data-ttu-id="46bee-103">建立 PsAzureApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="46bee-103">Creates an instance of PsAzureApiManagementContext.</span></span>

## <span data-ttu-id="46bee-104">語法</span><span class="sxs-lookup"><span data-stu-id="46bee-104">SYNTAX</span></span>

### <span data-ttu-id="46bee-105">CoNtextParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="46bee-105">ContextParameterSet (Default)</span></span>
```
New-AzApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46bee-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="46bee-106">ResourceIdParameterSet</span></span>
```
New-AzApiManagementContext -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46bee-107">描述</span><span class="sxs-lookup"><span data-stu-id="46bee-107">DESCRIPTION</span></span>
<span data-ttu-id="46bee-108">**New-AzApiManagementCoNtext** Cmdlet 會建立 **PsAzureApiManagementCoNtext 的實例**。</span><span class="sxs-lookup"><span data-stu-id="46bee-108">The **New-AzApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="46bee-109">上下文會用於所有 API 管理服務 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46bee-109">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="46bee-110">例子</span><span class="sxs-lookup"><span data-stu-id="46bee-110">EXAMPLES</span></span>

### <span data-ttu-id="46bee-111">範例 1：建立 PsApiManagementCoNtext 實例</span><span class="sxs-lookup"><span data-stu-id="46bee-111">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="46bee-112">此命令會建立 **PsApiManagementCoNtext 的實例**。</span><span class="sxs-lookup"><span data-stu-id="46bee-112">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="46bee-113">參數</span><span class="sxs-lookup"><span data-stu-id="46bee-113">PARAMETERS</span></span>

### <span data-ttu-id="46bee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46bee-114">-DefaultProfile</span></span>
<span data-ttu-id="46bee-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="46bee-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46bee-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46bee-116">-ResourceGroupName</span></span>
<span data-ttu-id="46bee-117">指定部署 API 管理服務的資源組名。</span><span class="sxs-lookup"><span data-stu-id="46bee-117">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46bee-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46bee-118">-ResourceId</span></span>
<span data-ttu-id="46bee-119">ApiManagement 服務的 Arm 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="46bee-119">Arm Resource Identifier of a ApiManagement service.</span></span> <span data-ttu-id="46bee-120">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="46bee-120">This parameter is required.</span></span>

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

### <span data-ttu-id="46bee-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="46bee-121">-ServiceName</span></span>
<span data-ttu-id="46bee-122">指定部署 API 管理服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="46bee-122">Specifies the name of the deployed API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46bee-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46bee-123">CommonParameters</span></span>
<span data-ttu-id="46bee-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="46bee-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46bee-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46bee-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46bee-126">輸入</span><span class="sxs-lookup"><span data-stu-id="46bee-126">INPUTS</span></span>

### <span data-ttu-id="46bee-127">System.String</span><span class="sxs-lookup"><span data-stu-id="46bee-127">System.String</span></span>

## <span data-ttu-id="46bee-128">輸出</span><span class="sxs-lookup"><span data-stu-id="46bee-128">OUTPUTS</span></span>

### <span data-ttu-id="46bee-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="46bee-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="46bee-130">筆記</span><span class="sxs-lookup"><span data-stu-id="46bee-130">NOTES</span></span>

## <span data-ttu-id="46bee-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="46bee-131">RELATED LINKS</span></span>
