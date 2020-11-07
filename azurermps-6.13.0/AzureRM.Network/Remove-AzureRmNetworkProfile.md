---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkProfile.md
ms.openlocfilehash: ebf2a58530f1dabe0e320dd78a38c63c86565c73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625782"
---
# <span data-ttu-id="8cf0d-101">Remove-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8cf0d-101">Remove-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="8cf0d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8cf0d-102">SYNOPSIS</span></span>
<span data-ttu-id="8cf0d-103">移除網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="8cf0d-103">Removes a network profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cf0d-104">句法</span><span class="sxs-lookup"><span data-stu-id="8cf0d-104">SYNTAX</span></span>

### <span data-ttu-id="8cf0d-105">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="8cf0d-105">RemoveByName</span></span>
```
Remove-AzureRmNetworkProfile -ResourceGroupName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cf0d-106">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cf0d-106">RemoveByNameParameterSet</span></span>
```
Remove-AzureRmNetworkProfile -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cf0d-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cf0d-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzureRmNetworkProfile -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cf0d-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cf0d-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzureRmNetworkProfile -InputObject <PSNetworkProfile> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cf0d-109">說明</span><span class="sxs-lookup"><span data-stu-id="8cf0d-109">DESCRIPTION</span></span>
<span data-ttu-id="8cf0d-110">如果沒有容器網路介面 (與已建立的容器網路介面 **配置** ) 相對，則 **Remove AzureRmNetworkProfile** Cmdlet 會移除網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="8cf0d-110">The **Remove-AzureRmNetworkProfile** cmdlet removes a network profile if no container network interfaces (as contrasted to a container network interface **configuration** ) have been created.</span></span>

## <span data-ttu-id="8cf0d-111">示例</span><span class="sxs-lookup"><span data-stu-id="8cf0d-111">EXAMPLES</span></span>

### <span data-ttu-id="8cf0d-112">範例1</span><span class="sxs-lookup"><span data-stu-id="8cf0d-112">Example 1</span></span>
```powershell
Remove-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="8cf0d-113">這會從資源群組 rg1 中移除名稱為 np1 的網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="8cf0d-113">This removes the network profile with name np1 from the resource group rg1.</span></span>

## <span data-ttu-id="8cf0d-114">參數</span><span class="sxs-lookup"><span data-stu-id="8cf0d-114">PARAMETERS</span></span>

### <span data-ttu-id="8cf0d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8cf0d-115">-AsJob</span></span>
<span data-ttu-id="8cf0d-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8cf0d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8cf0d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cf0d-117">-DefaultProfile</span></span>
<span data-ttu-id="8cf0d-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8cf0d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf0d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="8cf0d-119">-Force</span></span>
<span data-ttu-id="8cf0d-120">如果您想要刪除資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="8cf0d-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="8cf0d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8cf0d-121">-InputObject</span></span>
<span data-ttu-id="8cf0d-122">網路設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="8cf0d-122">Network profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkProfile
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8cf0d-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="8cf0d-123">-Name</span></span>
<span data-ttu-id="8cf0d-124">網路設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="8cf0d-124">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cf0d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8cf0d-125">-PassThru</span></span>
<span data-ttu-id="8cf0d-126">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="8cf0d-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8cf0d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cf0d-127">-ResourceGroupName</span></span>
<span data-ttu-id="8cf0d-128">網路設定檔的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="8cf0d-128">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cf0d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cf0d-129">-ResourceId</span></span>
<span data-ttu-id="8cf0d-130">網路設定檔的 Azure 資源管理員資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8cf0d-130">The Azure resource manager resource ID of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cf0d-131">-確認</span><span class="sxs-lookup"><span data-stu-id="8cf0d-131">-Confirm</span></span>
<span data-ttu-id="8cf0d-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8cf0d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cf0d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cf0d-133">-WhatIf</span></span>
<span data-ttu-id="8cf0d-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8cf0d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cf0d-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8cf0d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cf0d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cf0d-136">CommonParameters</span></span>
<span data-ttu-id="8cf0d-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8cf0d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cf0d-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8cf0d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cf0d-139">輸入</span><span class="sxs-lookup"><span data-stu-id="8cf0d-139">INPUTS</span></span>

### <span data-ttu-id="8cf0d-140">System.object</span><span class="sxs-lookup"><span data-stu-id="8cf0d-140">System.String</span></span>

## <span data-ttu-id="8cf0d-141">輸出</span><span class="sxs-lookup"><span data-stu-id="8cf0d-141">OUTPUTS</span></span>

### <span data-ttu-id="8cf0d-142">System.object</span><span class="sxs-lookup"><span data-stu-id="8cf0d-142">System.Boolean</span></span>

## <span data-ttu-id="8cf0d-143">筆記</span><span class="sxs-lookup"><span data-stu-id="8cf0d-143">NOTES</span></span>

## <span data-ttu-id="8cf0d-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="8cf0d-144">RELATED LINKS</span></span>
