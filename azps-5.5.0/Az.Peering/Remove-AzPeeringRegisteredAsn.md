---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d43fe033b58ba6295728bc0c21ddb1d853587b59
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141991"
---
# <span data-ttu-id="60a62-101">Remove-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="60a62-101">Remove-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="60a62-102">摘要</span><span class="sxs-lookup"><span data-stu-id="60a62-102">SYNOPSIS</span></span>
<span data-ttu-id="60a62-103">從父對等資源刪除或移除已註冊的 ASN。</span><span class="sxs-lookup"><span data-stu-id="60a62-103">Delete or remove a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="60a62-104">句法</span><span class="sxs-lookup"><span data-stu-id="60a62-104">SYNTAX</span></span>

### <span data-ttu-id="60a62-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="60a62-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60a62-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="60a62-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredAsn -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60a62-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="60a62-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60a62-108">說明</span><span class="sxs-lookup"><span data-stu-id="60a62-108">DESCRIPTION</span></span>
<span data-ttu-id="60a62-109">允許從父對等資源移除已註冊的 ASN。</span><span class="sxs-lookup"><span data-stu-id="60a62-109">Allows the removal of registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="60a62-110">示例</span><span class="sxs-lookup"><span data-stu-id="60a62-110">EXAMPLES</span></span>

### <span data-ttu-id="60a62-111">範例1</span><span class="sxs-lookup"><span data-stu-id="60a62-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredAsn -ResourceId $resourceId
```

<span data-ttu-id="60a62-112">依資源識別碼移除 registerd ASN。</span><span class="sxs-lookup"><span data-stu-id="60a62-112">Remove a registerd ASN by resource id.</span></span>

## <span data-ttu-id="60a62-113">參數</span><span class="sxs-lookup"><span data-stu-id="60a62-113">PARAMETERS</span></span>

### <span data-ttu-id="60a62-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60a62-114">-AsJob</span></span>
<span data-ttu-id="60a62-115">在背景中執行。</span><span class="sxs-lookup"><span data-stu-id="60a62-115">Run in the background.</span></span>

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

### <span data-ttu-id="60a62-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60a62-116">-DefaultProfile</span></span>
<span data-ttu-id="60a62-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="60a62-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60a62-118">-Force</span><span class="sxs-lookup"><span data-stu-id="60a62-118">-Force</span></span>
<span data-ttu-id="60a62-119">強制完成操作</span><span class="sxs-lookup"><span data-stu-id="60a62-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="60a62-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60a62-120">-InputObject</span></span>
<span data-ttu-id="60a62-121">使用 Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="60a62-121">Use a Get-AzPeeringServicePrefix</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60a62-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="60a62-122">-Name</span></span>
<span data-ttu-id="60a62-123">已註冊 ASN 的名稱</span><span class="sxs-lookup"><span data-stu-id="60a62-123">The name of the registered ASN</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60a62-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60a62-124">-PassThru</span></span>
<span data-ttu-id="60a62-125">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="60a62-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="60a62-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="60a62-126">-PeeringName</span></span>
<span data-ttu-id="60a62-127">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="60a62-127">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60a62-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60a62-128">-ResourceGroupName</span></span>
<span data-ttu-id="60a62-129">建立或使用現有的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="60a62-129">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60a62-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60a62-130">-ResourceId</span></span>
<span data-ttu-id="60a62-131">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="60a62-131">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60a62-132">-確認</span><span class="sxs-lookup"><span data-stu-id="60a62-132">-Confirm</span></span>
<span data-ttu-id="60a62-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="60a62-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60a62-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60a62-134">-WhatIf</span></span>
<span data-ttu-id="60a62-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="60a62-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60a62-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="60a62-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60a62-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60a62-137">CommonParameters</span></span>
<span data-ttu-id="60a62-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="60a62-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60a62-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="60a62-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60a62-140">輸入</span><span class="sxs-lookup"><span data-stu-id="60a62-140">INPUTS</span></span>

### <span data-ttu-id="60a62-141">PSPeeringServicePrefix 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="60a62-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="60a62-142">System.object</span><span class="sxs-lookup"><span data-stu-id="60a62-142">System.String</span></span>

## <span data-ttu-id="60a62-143">輸出</span><span class="sxs-lookup"><span data-stu-id="60a62-143">OUTPUTS</span></span>

### <span data-ttu-id="60a62-144">System.object</span><span class="sxs-lookup"><span data-stu-id="60a62-144">System.Boolean</span></span>

## <span data-ttu-id="60a62-145">筆記</span><span class="sxs-lookup"><span data-stu-id="60a62-145">NOTES</span></span>

## <span data-ttu-id="60a62-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="60a62-146">RELATED LINKS</span></span>
