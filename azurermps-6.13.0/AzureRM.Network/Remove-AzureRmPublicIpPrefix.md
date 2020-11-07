---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpPrefix.md
ms.openlocfilehash: e361e4d3c4daec88ddb35fa7973b65f630dcc390
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625777"
---
# <span data-ttu-id="4ff6b-101">Remove-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4ff6b-101">Remove-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="4ff6b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4ff6b-102">SYNOPSIS</span></span>
<span data-ttu-id="4ff6b-103">移除公用 IP 首碼</span><span class="sxs-lookup"><span data-stu-id="4ff6b-103">Removes a public IP prefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ff6b-104">句法</span><span class="sxs-lookup"><span data-stu-id="4ff6b-104">SYNTAX</span></span>

### <span data-ttu-id="4ff6b-105">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ff6b-105">RemoveByNameParameterSet</span></span>
```
Remove-AzureRmPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ff6b-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ff6b-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzureRmPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ff6b-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ff6b-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzureRmPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ff6b-108">說明</span><span class="sxs-lookup"><span data-stu-id="4ff6b-108">DESCRIPTION</span></span>
<span data-ttu-id="4ff6b-109">\* \* Remove-AzureRmPublicIpPrefix Cmdlet 會移除 Azure 公用 IP 首碼，只要沒有任何指派公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="4ff6b-109">The \*\*Remove-AzureRmPublicIpPrefix cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="4ff6b-110">示例</span><span class="sxs-lookup"><span data-stu-id="4ff6b-110">EXAMPLES</span></span>

### <span data-ttu-id="4ff6b-111">範例1</span><span class="sxs-lookup"><span data-stu-id="4ff6b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="4ff6b-112">從 [資源群組] $rgName 移除名稱 $prefixName 的公用 IP 首碼</span><span class="sxs-lookup"><span data-stu-id="4ff6b-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="4ff6b-113">參數</span><span class="sxs-lookup"><span data-stu-id="4ff6b-113">PARAMETERS</span></span>

### <span data-ttu-id="4ff6b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ff6b-114">-AsJob</span></span>
<span data-ttu-id="4ff6b-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4ff6b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4ff6b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ff6b-116">-DefaultProfile</span></span>
<span data-ttu-id="4ff6b-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4ff6b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ff6b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4ff6b-118">-Force</span></span>
<span data-ttu-id="4ff6b-119">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="4ff6b-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4ff6b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ff6b-120">-InputObject</span></span>
<span data-ttu-id="4ff6b-121">PublicIpPrefix 物件</span><span class="sxs-lookup"><span data-stu-id="4ff6b-121">A PublicIpPrefix object</span></span>

```yaml
Type: PSPublicIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ff6b-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="4ff6b-122">-Name</span></span>
<span data-ttu-id="4ff6b-123">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="4ff6b-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ff6b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ff6b-124">-PassThru</span></span>
<span data-ttu-id="4ff6b-125">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="4ff6b-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4ff6b-126">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="4ff6b-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4ff6b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ff6b-127">-ResourceGroupName</span></span>
<span data-ttu-id="4ff6b-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ff6b-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ff6b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ff6b-129">-ResourceId</span></span>
<span data-ttu-id="4ff6b-130">要移除之資源的 resourceId</span><span class="sxs-lookup"><span data-stu-id="4ff6b-130">The resourceId for the resource to remove</span></span>

```yaml
Type: String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ff6b-131">-確認</span><span class="sxs-lookup"><span data-stu-id="4ff6b-131">-Confirm</span></span>
<span data-ttu-id="4ff6b-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4ff6b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ff6b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ff6b-133">-WhatIf</span></span>
<span data-ttu-id="4ff6b-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4ff6b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ff6b-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4ff6b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ff6b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ff6b-136">CommonParameters</span></span>
<span data-ttu-id="4ff6b-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4ff6b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4ff6b-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4ff6b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ff6b-139">輸入</span><span class="sxs-lookup"><span data-stu-id="4ff6b-139">INPUTS</span></span>

### <span data-ttu-id="4ff6b-140">System.object</span><span class="sxs-lookup"><span data-stu-id="4ff6b-140">System.String</span></span>
<span data-ttu-id="4ff6b-141">PSPublicIpPrefix 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4ff6b-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="4ff6b-142">輸出</span><span class="sxs-lookup"><span data-stu-id="4ff6b-142">OUTPUTS</span></span>

### <span data-ttu-id="4ff6b-143">System.object</span><span class="sxs-lookup"><span data-stu-id="4ff6b-143">System.Object</span></span>

## <span data-ttu-id="4ff6b-144">筆記</span><span class="sxs-lookup"><span data-stu-id="4ff6b-144">NOTES</span></span>

## <span data-ttu-id="4ff6b-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ff6b-145">RELATED LINKS</span></span>
