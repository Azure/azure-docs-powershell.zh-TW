---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
ms.openlocfilehash: c95fe4a977c70964cf8b4dab86985d79315d3141
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916507"
---
# <span data-ttu-id="8f221-101">Get-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="8f221-101">Get-AzManagedApplication</span></span>

## <span data-ttu-id="8f221-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8f221-102">SYNOPSIS</span></span>
<span data-ttu-id="8f221-103">獲得受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="8f221-103">Gets managed applications</span></span>

## <span data-ttu-id="8f221-104">語法</span><span class="sxs-lookup"><span data-stu-id="8f221-104">SYNTAX</span></span>

### <span data-ttu-id="8f221-105">GetBySubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="8f221-105">GetBySubscription (Default)</span></span>
```
Get-AzManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f221-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8f221-106">GetByNameAndResourceGroup</span></span>
```
Get-AzManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f221-107">GetById</span><span class="sxs-lookup"><span data-stu-id="8f221-107">GetById</span></span>
```
Get-AzManagedApplication -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8f221-108">描述</span><span class="sxs-lookup"><span data-stu-id="8f221-108">DESCRIPTION</span></span>
<span data-ttu-id="8f221-109">**Get-AzManagedApplication** Cmdlet 取得受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="8f221-109">The **Get-AzManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="8f221-110">例子</span><span class="sxs-lookup"><span data-stu-id="8f221-110">EXAMPLES</span></span>

### <span data-ttu-id="8f221-111">範例 1：在資源群組下取得所有受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="8f221-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="8f221-112">此命令在資源群組 「MyRG」 下獲得受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="8f221-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="8f221-113">範例 2：取得所有受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="8f221-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzManagedApplication
```

<span data-ttu-id="8f221-114">此命令會取得目前訂閱下的所有受管理應用程式</span><span class="sxs-lookup"><span data-stu-id="8f221-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="8f221-115">參數</span><span class="sxs-lookup"><span data-stu-id="8f221-115">PARAMETERS</span></span>

### <span data-ttu-id="8f221-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8f221-116">-ApiVersion</span></span>
<span data-ttu-id="8f221-117">設定時，表示要使用資源提供者 API 的版本。</span><span class="sxs-lookup"><span data-stu-id="8f221-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="8f221-118">如果未指定，API 版本會自動判斷為最新可用。</span><span class="sxs-lookup"><span data-stu-id="8f221-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f221-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f221-119">-DefaultProfile</span></span>
<span data-ttu-id="8f221-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8f221-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f221-121">-Id</span><span class="sxs-lookup"><span data-stu-id="8f221-121">-Id</span></span>
<span data-ttu-id="8f221-122">完整受管理的應用程式識別碼，包括訂閱。</span><span class="sxs-lookup"><span data-stu-id="8f221-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="8f221-123">例如/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="8f221-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f221-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="8f221-124">-Name</span></span>
<span data-ttu-id="8f221-125">受管理的應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="8f221-125">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f221-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="8f221-126">-Pre</span></span>
<span data-ttu-id="8f221-127">設定之後，表示當系統自動決定要使用哪個版本時，Cmdlet 應該使用測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="8f221-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f221-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f221-128">-ResourceGroupName</span></span>
<span data-ttu-id="8f221-129">資源組名。</span><span class="sxs-lookup"><span data-stu-id="8f221-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f221-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f221-130">CommonParameters</span></span>
<span data-ttu-id="8f221-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8f221-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f221-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f221-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f221-133">輸入</span><span class="sxs-lookup"><span data-stu-id="8f221-133">INPUTS</span></span>

### <span data-ttu-id="8f221-134">System.String</span><span class="sxs-lookup"><span data-stu-id="8f221-134">System.String</span></span>

## <span data-ttu-id="8f221-135">輸出</span><span class="sxs-lookup"><span data-stu-id="8f221-135">OUTPUTS</span></span>

### <span data-ttu-id="8f221-136">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="8f221-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8f221-137">筆記</span><span class="sxs-lookup"><span data-stu-id="8f221-137">NOTES</span></span>

## <span data-ttu-id="8f221-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f221-138">RELATED LINKS</span></span>
