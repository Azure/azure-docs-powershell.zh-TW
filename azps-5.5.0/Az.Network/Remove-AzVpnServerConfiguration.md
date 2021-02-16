---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
ms.openlocfilehash: 5d4fa487210b732e0121a01f7cc5fa392ebfb68c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128714"
---
# <span data-ttu-id="06b10-101">Remove-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="06b10-101">Remove-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="06b10-102">摘要</span><span class="sxs-lookup"><span data-stu-id="06b10-102">SYNOPSIS</span></span>
<span data-ttu-id="06b10-103">移除現有的 VpnServerConfiguration。</span><span class="sxs-lookup"><span data-stu-id="06b10-103">Removes an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="06b10-104">句法</span><span class="sxs-lookup"><span data-stu-id="06b10-104">SYNTAX</span></span>

### <span data-ttu-id="06b10-105">ByVpnServerConfigurationName (預設) </span><span class="sxs-lookup"><span data-stu-id="06b10-105">ByVpnServerConfigurationName (Default)</span></span>
```
Remove-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06b10-106">ByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="06b10-106">ByVpnServerConfigurationObject</span></span>
```
Remove-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06b10-107">ByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="06b10-107">ByVpnServerConfigurationResourceId</span></span>
```
Remove-AzVpnServerConfiguration -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06b10-108">說明</span><span class="sxs-lookup"><span data-stu-id="06b10-108">DESCRIPTION</span></span>
<span data-ttu-id="06b10-109">{{填入描述}}</span><span class="sxs-lookup"><span data-stu-id="06b10-109">{{Fill in the Description}}</span></span>

## <span data-ttu-id="06b10-110">示例</span><span class="sxs-lookup"><span data-stu-id="06b10-110">EXAMPLES</span></span>

### <span data-ttu-id="06b10-111">範例1</span><span class="sxs-lookup"><span data-stu-id="06b10-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -Force -PassThru
```

<span data-ttu-id="06b10-112">上述命令會移除現有的 VpnServerConfiguration。</span><span class="sxs-lookup"><span data-stu-id="06b10-112">The above command will remove an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="06b10-113">參數</span><span class="sxs-lookup"><span data-stu-id="06b10-113">PARAMETERS</span></span>

### <span data-ttu-id="06b10-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06b10-114">-DefaultProfile</span></span>
<span data-ttu-id="06b10-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="06b10-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06b10-116">-Force</span><span class="sxs-lookup"><span data-stu-id="06b10-116">-Force</span></span>
<span data-ttu-id="06b10-117">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="06b10-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="06b10-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06b10-118">-InputObject</span></span>
<span data-ttu-id="06b10-119">要刪除的 vpnServerConfiguration 物件。</span><span class="sxs-lookup"><span data-stu-id="06b10-119">The vpnServerConfiguration object to be deleted.</span></span>

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

### <span data-ttu-id="06b10-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="06b10-120">-Name</span></span>
<span data-ttu-id="06b10-121">VpnServerConfiguration 的名稱。</span><span class="sxs-lookup"><span data-stu-id="06b10-121">The vpnServerConfiguration name.</span></span>

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

### <span data-ttu-id="06b10-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06b10-122">-PassThru</span></span>
<span data-ttu-id="06b10-123">傳回代表執行此作業之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="06b10-123">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="06b10-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06b10-124">-ResourceGroupName</span></span>
<span data-ttu-id="06b10-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="06b10-125">The resource group name.</span></span>

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

### <span data-ttu-id="06b10-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06b10-126">-ResourceId</span></span>
<span data-ttu-id="06b10-127">要刪除之 vpnServerConfiguration 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="06b10-127">The Azure resource ID for the vpnServerConfiguration to be deleted.</span></span>

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

### <span data-ttu-id="06b10-128">-確認</span><span class="sxs-lookup"><span data-stu-id="06b10-128">-Confirm</span></span>
<span data-ttu-id="06b10-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="06b10-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06b10-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06b10-130">-WhatIf</span></span>
<span data-ttu-id="06b10-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="06b10-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06b10-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06b10-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06b10-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06b10-133">CommonParameters</span></span>
<span data-ttu-id="06b10-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="06b10-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06b10-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="06b10-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06b10-136">輸入</span><span class="sxs-lookup"><span data-stu-id="06b10-136">INPUTS</span></span>

### <span data-ttu-id="06b10-137">PSVpnServerConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="06b10-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="06b10-138">System.object</span><span class="sxs-lookup"><span data-stu-id="06b10-138">System.String</span></span>

## <span data-ttu-id="06b10-139">輸出</span><span class="sxs-lookup"><span data-stu-id="06b10-139">OUTPUTS</span></span>

### <span data-ttu-id="06b10-140">System.object</span><span class="sxs-lookup"><span data-stu-id="06b10-140">System.Boolean</span></span>

## <span data-ttu-id="06b10-141">筆記</span><span class="sxs-lookup"><span data-stu-id="06b10-141">NOTES</span></span>

## <span data-ttu-id="06b10-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="06b10-142">RELATED LINKS</span></span>
