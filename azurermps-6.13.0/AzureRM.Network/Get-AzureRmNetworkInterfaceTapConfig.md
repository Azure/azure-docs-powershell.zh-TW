---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceTapConfig.md
ms.openlocfilehash: 2f6c4f410c7d4f92c8dcd911e0c113f2a91b304c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626539"
---
# <span data-ttu-id="ae7bb-101">Get-AzureRmNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="ae7bb-101">Get-AzureRmNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="ae7bb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ae7bb-102">SYNOPSIS</span></span>
<span data-ttu-id="ae7bb-103">取得攻絲配置資源。</span><span class="sxs-lookup"><span data-stu-id="ae7bb-103">Gets a Tap configuration resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae7bb-104">句法</span><span class="sxs-lookup"><span data-stu-id="ae7bb-104">SYNTAX</span></span>

### <span data-ttu-id="ae7bb-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ae7bb-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzureRmNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae7bb-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae7bb-106">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae7bb-107">說明</span><span class="sxs-lookup"><span data-stu-id="ae7bb-107">DESCRIPTION</span></span>
<span data-ttu-id="ae7bb-108">AzureRmNetworkInterfaceTapConfig Cmdlet 會針對特定資源群組、網路介面，並在資源群組和網路介面中，針對指定的資源群組、網路介面，以及攻絲配置的清單， **取得** Azure 攻絲設定。</span><span class="sxs-lookup"><span data-stu-id="ae7bb-108">The **Get-AzureRmNetworkInterfaceTapConfig** cmdlet gets an Azure Tap Configuration for a given resource group, network interface and tap configuration name or list of tap configurations in a resource group and network interface.</span></span>

## <span data-ttu-id="ae7bb-109">示例</span><span class="sxs-lookup"><span data-stu-id="ae7bb-109">EXAMPLES</span></span>

### <span data-ttu-id="ae7bb-110">範例1：取得指定網路介面的所有攻絲設定</span><span class="sxs-lookup"><span data-stu-id="ae7bb-110">Example 1: Get all tap configurations for a given network interface</span></span>
```
PS C:\>Get-AzureRmNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

<span data-ttu-id="ae7bb-111">這個命令會針對指定的網路介面，分路器所新增的配置。</span><span class="sxs-lookup"><span data-stu-id="ae7bb-111">This command gets tap configurations added for the given network interface.</span></span>

### <span data-ttu-id="ae7bb-112">範例2：取得特定的攻絲配置</span><span class="sxs-lookup"><span data-stu-id="ae7bb-112">Example 2: Get a given tap configuration</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

<span data-ttu-id="ae7bb-113">這個命令會針對指定的網路介面，取得已新增的特定分路配置。</span><span class="sxs-lookup"><span data-stu-id="ae7bb-113">This command gets specific tap configuration added for the given network interface.</span></span>

## <span data-ttu-id="ae7bb-114">參數</span><span class="sxs-lookup"><span data-stu-id="ae7bb-114">PARAMETERS</span></span>

### <span data-ttu-id="ae7bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae7bb-115">-DefaultProfile</span></span>
<span data-ttu-id="ae7bb-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ae7bb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae7bb-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="ae7bb-117">-Name</span></span>
<span data-ttu-id="ae7bb-118">特定攻絲配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae7bb-118">Name of the specific tap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae7bb-119">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="ae7bb-119">-NetworkInterfaceName</span></span>
<span data-ttu-id="ae7bb-120">網路介面名稱。</span><span class="sxs-lookup"><span data-stu-id="ae7bb-120">The Network Interface name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae7bb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae7bb-121">-ResourceGroupName</span></span>
<span data-ttu-id="ae7bb-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae7bb-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae7bb-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae7bb-123">-ResourceId</span></span>
<span data-ttu-id="ae7bb-124">TapConfiguration 資源的 ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae7bb-124">ResourceId of the TapConfiguration resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae7bb-125">-確認</span><span class="sxs-lookup"><span data-stu-id="ae7bb-125">-Confirm</span></span>
<span data-ttu-id="ae7bb-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ae7bb-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae7bb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae7bb-127">-WhatIf</span></span>
<span data-ttu-id="ae7bb-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ae7bb-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae7bb-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ae7bb-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae7bb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae7bb-130">CommonParameters</span></span>
<span data-ttu-id="ae7bb-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ae7bb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae7bb-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ae7bb-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae7bb-133">輸入</span><span class="sxs-lookup"><span data-stu-id="ae7bb-133">INPUTS</span></span>

### <span data-ttu-id="ae7bb-134">System.object</span><span class="sxs-lookup"><span data-stu-id="ae7bb-134">System.String</span></span>

## <span data-ttu-id="ae7bb-135">輸出</span><span class="sxs-lookup"><span data-stu-id="ae7bb-135">OUTPUTS</span></span>

### <span data-ttu-id="ae7bb-136">PSNetworkInterfaceTapConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ae7bb-136">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="ae7bb-137">筆記</span><span class="sxs-lookup"><span data-stu-id="ae7bb-137">NOTES</span></span>

## <span data-ttu-id="ae7bb-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="ae7bb-138">RELATED LINKS</span></span>
