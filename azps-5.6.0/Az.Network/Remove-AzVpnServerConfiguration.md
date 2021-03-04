---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
ms.openlocfilehash: f5451b2c3af331f0086f39f46028aff1d33bf002
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911625"
---
# <span data-ttu-id="56245-101">Remove-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="56245-101">Remove-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="56245-102">簡介</span><span class="sxs-lookup"><span data-stu-id="56245-102">SYNOPSIS</span></span>
<span data-ttu-id="56245-103">移除現有的 VpnServerConfiguration。</span><span class="sxs-lookup"><span data-stu-id="56245-103">Removes an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="56245-104">語法</span><span class="sxs-lookup"><span data-stu-id="56245-104">SYNTAX</span></span>

### <span data-ttu-id="56245-105">By VpnServerConfigurationName (預設) </span><span class="sxs-lookup"><span data-stu-id="56245-105">ByVpnServerConfigurationName (Default)</span></span>
```
Remove-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56245-106">By VpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="56245-106">ByVpnServerConfigurationObject</span></span>
```
Remove-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56245-107">By VpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="56245-107">ByVpnServerConfigurationResourceId</span></span>
```
Remove-AzVpnServerConfiguration -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56245-108">描述</span><span class="sxs-lookup"><span data-stu-id="56245-108">DESCRIPTION</span></span>
<span data-ttu-id="56245-109">{{填寫 Description}}</span><span class="sxs-lookup"><span data-stu-id="56245-109">{{Fill in the Description}}</span></span>

## <span data-ttu-id="56245-110">例子</span><span class="sxs-lookup"><span data-stu-id="56245-110">EXAMPLES</span></span>

### <span data-ttu-id="56245-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="56245-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -Force -PassThru
```

<span data-ttu-id="56245-112">上述命令會移除現有的 VpnServerConfiguration。</span><span class="sxs-lookup"><span data-stu-id="56245-112">The above command will remove an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="56245-113">參數</span><span class="sxs-lookup"><span data-stu-id="56245-113">PARAMETERS</span></span>

### <span data-ttu-id="56245-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56245-114">-DefaultProfile</span></span>
<span data-ttu-id="56245-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="56245-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56245-116">-強制</span><span class="sxs-lookup"><span data-stu-id="56245-116">-Force</span></span>
<span data-ttu-id="56245-117">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="56245-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="56245-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56245-118">-InputObject</span></span>
<span data-ttu-id="56245-119">要刪除的 vpnServerConfiguration 物件。</span><span class="sxs-lookup"><span data-stu-id="56245-119">The vpnServerConfiguration object to be deleted.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObject
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56245-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="56245-120">-Name</span></span>
<span data-ttu-id="56245-121">vpnServerConfiguration 名稱。</span><span class="sxs-lookup"><span data-stu-id="56245-121">The vpnServerConfiguration name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationName
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56245-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="56245-122">-PassThru</span></span>
<span data-ttu-id="56245-123">會返回代表執行此作業之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="56245-123">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="56245-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56245-124">-ResourceGroupName</span></span>
<span data-ttu-id="56245-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="56245-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56245-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56245-126">-ResourceId</span></span>
<span data-ttu-id="56245-127">要刪除 vpnServerConfiguration 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="56245-127">The Azure resource ID for the vpnServerConfiguration to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationResourceId
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56245-128">-確認</span><span class="sxs-lookup"><span data-stu-id="56245-128">-Confirm</span></span>
<span data-ttu-id="56245-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="56245-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56245-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56245-130">-WhatIf</span></span>
<span data-ttu-id="56245-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="56245-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56245-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="56245-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56245-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56245-133">CommonParameters</span></span>
<span data-ttu-id="56245-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="56245-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56245-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="56245-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56245-136">輸入</span><span class="sxs-lookup"><span data-stu-id="56245-136">INPUTS</span></span>

### <span data-ttu-id="56245-137">Microsoft.Azure.Commands.Network.models.PS VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="56245-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="56245-138">System.String</span><span class="sxs-lookup"><span data-stu-id="56245-138">System.String</span></span>

## <span data-ttu-id="56245-139">輸出</span><span class="sxs-lookup"><span data-stu-id="56245-139">OUTPUTS</span></span>

### <span data-ttu-id="56245-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="56245-140">System.Boolean</span></span>

## <span data-ttu-id="56245-141">筆記</span><span class="sxs-lookup"><span data-stu-id="56245-141">NOTES</span></span>

## <span data-ttu-id="56245-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="56245-142">RELATED LINKS</span></span>
