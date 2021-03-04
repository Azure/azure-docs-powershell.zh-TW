---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
ms.openlocfilehash: f1f71d188a6b25146103fe3fe5d91b8ba53eaaf8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910377"
---
# <span data-ttu-id="350a4-101">Get-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="350a4-101">Get-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="350a4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="350a4-102">SYNOPSIS</span></span>
<span data-ttu-id="350a4-103">獲得受管理的應用程式定義</span><span class="sxs-lookup"><span data-stu-id="350a4-103">Gets managed application definitions</span></span>

## <span data-ttu-id="350a4-104">語法</span><span class="sxs-lookup"><span data-stu-id="350a4-104">SYNTAX</span></span>

### <span data-ttu-id="350a4-105">GetByNameAndResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="350a4-105">GetByNameAndResourceGroup (Default)</span></span>
```
Get-AzManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="350a4-106">GetById</span><span class="sxs-lookup"><span data-stu-id="350a4-106">GetById</span></span>
```
Get-AzManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="350a4-107">描述</span><span class="sxs-lookup"><span data-stu-id="350a4-107">DESCRIPTION</span></span>
<span data-ttu-id="350a4-108">**Get-AzManagedApplicationDefinition** Cmdlet 取得受管理的應用程式定義</span><span class="sxs-lookup"><span data-stu-id="350a4-108">The **Get-AzManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="350a4-109">例子</span><span class="sxs-lookup"><span data-stu-id="350a4-109">EXAMPLES</span></span>

### <span data-ttu-id="350a4-110">範例 1：在資源群組下取得所有受管理的應用程式定義</span><span class="sxs-lookup"><span data-stu-id="350a4-110">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="350a4-111">此命令會獲得資源群組 「MyRG」 下的受管理應用程式定義</span><span class="sxs-lookup"><span data-stu-id="350a4-111">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="350a4-112">範例 2：取得受管理的應用程式定義</span><span class="sxs-lookup"><span data-stu-id="350a4-112">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="350a4-113">此命令會獲得資源群組 "MyRG" 下的受管理應用程式定義 "myManagedAppDef"</span><span class="sxs-lookup"><span data-stu-id="350a4-113">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="350a4-114">參數</span><span class="sxs-lookup"><span data-stu-id="350a4-114">PARAMETERS</span></span>

### <span data-ttu-id="350a4-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="350a4-115">-ApiVersion</span></span>
<span data-ttu-id="350a4-116">設定時，表示要使用資源提供者 API 的版本。</span><span class="sxs-lookup"><span data-stu-id="350a4-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="350a4-117">如果未指定，API 版本會自動判斷為最新可用。</span><span class="sxs-lookup"><span data-stu-id="350a4-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="350a4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="350a4-118">-DefaultProfile</span></span>
<span data-ttu-id="350a4-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="350a4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="350a4-120">-Id</span><span class="sxs-lookup"><span data-stu-id="350a4-120">-Id</span></span>
<span data-ttu-id="350a4-121">完整受管理的應用程式定義識別碼，包括訂閱。</span><span class="sxs-lookup"><span data-stu-id="350a4-121">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="350a4-122">例如/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="350a4-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationDefinitionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="350a4-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="350a4-123">-Name</span></span>
<span data-ttu-id="350a4-124">受管理的應用程式定義名稱。</span><span class="sxs-lookup"><span data-stu-id="350a4-124">The managed application definition name.</span></span>

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

### <span data-ttu-id="350a4-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="350a4-125">-Pre</span></span>
<span data-ttu-id="350a4-126">設定之後，表示當系統自動決定要使用哪個版本時，Cmdlet 應該使用測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="350a4-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="350a4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="350a4-127">-ResourceGroupName</span></span>
<span data-ttu-id="350a4-128">資源組名。</span><span class="sxs-lookup"><span data-stu-id="350a4-128">The resource group name.</span></span>

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

### <span data-ttu-id="350a4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="350a4-129">CommonParameters</span></span>
<span data-ttu-id="350a4-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="350a4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="350a4-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="350a4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="350a4-132">輸入</span><span class="sxs-lookup"><span data-stu-id="350a4-132">INPUTS</span></span>

### <span data-ttu-id="350a4-133">System.String</span><span class="sxs-lookup"><span data-stu-id="350a4-133">System.String</span></span>

## <span data-ttu-id="350a4-134">輸出</span><span class="sxs-lookup"><span data-stu-id="350a4-134">OUTPUTS</span></span>

### <span data-ttu-id="350a4-135">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="350a4-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="350a4-136">筆記</span><span class="sxs-lookup"><span data-stu-id="350a4-136">NOTES</span></span>

## <span data-ttu-id="350a4-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="350a4-137">RELATED LINKS</span></span>
