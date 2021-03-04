---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
ms.openlocfilehash: 3fda360369615c28647769e6bc5aeb0af71e0e35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915997"
---
# <span data-ttu-id="325a7-101">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="325a7-101">Remove-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="325a7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="325a7-102">SYNOPSIS</span></span>
<span data-ttu-id="325a7-103">刪除 Azure SecurityPartnerProvider。</span><span class="sxs-lookup"><span data-stu-id="325a7-103">Deletes an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="325a7-104">語法</span><span class="sxs-lookup"><span data-stu-id="325a7-104">SYNTAX</span></span>

### <span data-ttu-id="325a7-105">SecurityPartnerProviderNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="325a7-105">SecurityPartnerProviderNameParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="325a7-106">SecurityPartnerProviderInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="325a7-106">SecurityPartnerProviderInputObjectParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="325a7-107">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="325a7-107">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="325a7-108">描述</span><span class="sxs-lookup"><span data-stu-id="325a7-108">DESCRIPTION</span></span>
<span data-ttu-id="325a7-109">**Remove-AzSecurityPartnerProvider Cmdlet** 會刪除 Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="325a7-109">The **Remove-AzSecurityPartnerProvider** cmdlet deletes an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="325a7-110">例子</span><span class="sxs-lookup"><span data-stu-id="325a7-110">EXAMPLES</span></span>

### <span data-ttu-id="325a7-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="325a7-111">Example 1</span></span>
```powershell
Remove-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```

## <span data-ttu-id="325a7-112">參數</span><span class="sxs-lookup"><span data-stu-id="325a7-112">PARAMETERS</span></span>

### <span data-ttu-id="325a7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="325a7-113">-AsJob</span></span>
<span data-ttu-id="325a7-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="325a7-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="325a7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="325a7-115">-DefaultProfile</span></span>
<span data-ttu-id="325a7-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="325a7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="325a7-117">-強制</span><span class="sxs-lookup"><span data-stu-id="325a7-117">-Force</span></span>
<span data-ttu-id="325a7-118">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="325a7-118">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="325a7-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="325a7-119">-Name</span></span>
<span data-ttu-id="325a7-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="325a7-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="325a7-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="325a7-121">-PassThru</span></span>
<span data-ttu-id="325a7-122">會返回代表執行此作業之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="325a7-122">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="325a7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="325a7-123">-ResourceGroupName</span></span>
<span data-ttu-id="325a7-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="325a7-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="325a7-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="325a7-125">-ResourceId</span></span>
<span data-ttu-id="325a7-126">SecurityPartnerProvider 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="325a7-126">The securityPartnerProvider resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="325a7-127">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="325a7-127">-SecurityPartnerProvider</span></span>
<span data-ttu-id="325a7-128">SecurityPartnerProvider 輸入物件。</span><span class="sxs-lookup"><span data-stu-id="325a7-128">The securityPartnerProvider input object.</span></span>

```yaml
Type: PSSecurityPartnerProvider
Parameter Sets: SecurityPartnerProviderInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="325a7-129">-確認</span><span class="sxs-lookup"><span data-stu-id="325a7-129">-Confirm</span></span>
<span data-ttu-id="325a7-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="325a7-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="325a7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="325a7-131">-WhatIf</span></span>
<span data-ttu-id="325a7-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="325a7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="325a7-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="325a7-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="325a7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="325a7-134">CommonParameters</span></span>
<span data-ttu-id="325a7-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="325a7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="325a7-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="325a7-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="325a7-137">輸入</span><span class="sxs-lookup"><span data-stu-id="325a7-137">INPUTS</span></span>

### <span data-ttu-id="325a7-138">System.String</span><span class="sxs-lookup"><span data-stu-id="325a7-138">System.String</span></span>

### <span data-ttu-id="325a7-139">Microsoft.Azure.Commands.Network.models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="325a7-139">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="325a7-140">輸出</span><span class="sxs-lookup"><span data-stu-id="325a7-140">OUTPUTS</span></span>

### <span data-ttu-id="325a7-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="325a7-141">System.Boolean</span></span>

## <span data-ttu-id="325a7-142">筆記</span><span class="sxs-lookup"><span data-stu-id="325a7-142">NOTES</span></span>

## <span data-ttu-id="325a7-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="325a7-143">RELATED LINKS</span></span>
