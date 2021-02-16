---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: cd9270d724e0e1523c3ee621cb58fa28a2f4bc66
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131106"
---
# <span data-ttu-id="8d584-101">Set-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="8d584-101">Set-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="8d584-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8d584-102">SYNOPSIS</span></span>
<span data-ttu-id="8d584-103">[更新 DNS 區域] 群組</span><span class="sxs-lookup"><span data-stu-id="8d584-103">Updates DNS zone group</span></span>

## <span data-ttu-id="8d584-104">句法</span><span class="sxs-lookup"><span data-stu-id="8d584-104">SYNTAX</span></span>

```
Set-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d584-105">說明</span><span class="sxs-lookup"><span data-stu-id="8d584-105">DESCRIPTION</span></span>
<span data-ttu-id="8d584-106">**AzPrivateDnsZoneGroup** Cmdlet 會更新 DNS 區域群組。</span><span class="sxs-lookup"><span data-stu-id="8d584-106">The **Set-AzPrivateDnsZoneGroup** cmdlet updates DNS zone group.</span></span>

## <span data-ttu-id="8d584-107">示例</span><span class="sxs-lookup"><span data-stu-id="8d584-107">EXAMPLES</span></span>

### <span data-ttu-id="8d584-108">範例1</span><span class="sxs-lookup"><span data-stu-id="8d584-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPrivateDnsZoneGroup -ResourceGroupName rg -PrivateEndpointName my-pr-endpoint -name dnsgroup1

Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/my-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test.vault.azure.com",
                            "RecordSets": []
                          }
                        ]

PS C:\> $zone1 = Get-AzPrivateDnsZone -ResourceGroupName rg -Name "test1.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name test1-vault-azure-com -PrivateDnsZoneId $zone1.ResourceId
PS C:\> Set-AzPrivateDnsZoneGroup -ResourceGroupName rg -PrivateEndpointName my-pr-endpoint -name dnsgroup1 -PrivateDnsZoneConfig $config -Force

Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/my-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test1-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test1.vault.azure.com",
                            "RecordSets": []
                          }
                        ]
```

<span data-ttu-id="8d584-109">上述範例會使用新的 dnsconfig 更新名為 dnsgroup1 的 DNS 區域群組，以取得另一個 DNS 區域的連結。</span><span class="sxs-lookup"><span data-stu-id="8d584-109">Above example updates DNS zone group named dnsgroup1 with a new dnsconfig which links to another DNS zone.</span></span>

## <span data-ttu-id="8d584-110">參數</span><span class="sxs-lookup"><span data-stu-id="8d584-110">PARAMETERS</span></span>

### <span data-ttu-id="8d584-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d584-111">-AsJob</span></span>
<span data-ttu-id="8d584-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8d584-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8d584-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d584-113">-DefaultProfile</span></span>
<span data-ttu-id="8d584-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8d584-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d584-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="8d584-115">-Name</span></span>
<span data-ttu-id="8d584-116">專用 dns 區域群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d584-116">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d584-117">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="8d584-117">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="8d584-118">私人 dns 區域群組的專用 dns 區域設定集合。</span><span class="sxs-lookup"><span data-stu-id="8d584-118">A collection of private dns zone configurations of the private dns zone group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d584-119">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="8d584-119">-PrivateEndpointName</span></span>
<span data-ttu-id="8d584-120">私人端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d584-120">The name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d584-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d584-121">-ResourceGroupName</span></span>
<span data-ttu-id="8d584-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d584-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d584-123">-確認</span><span class="sxs-lookup"><span data-stu-id="8d584-123">-Confirm</span></span>
<span data-ttu-id="8d584-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8d584-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d584-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d584-125">-WhatIf</span></span>
<span data-ttu-id="8d584-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8d584-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d584-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8d584-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d584-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d584-128">CommonParameters</span></span>
<span data-ttu-id="8d584-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8d584-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d584-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8d584-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d584-131">輸入</span><span class="sxs-lookup"><span data-stu-id="8d584-131">INPUTS</span></span>

### <span data-ttu-id="8d584-132">System.object</span><span class="sxs-lookup"><span data-stu-id="8d584-132">System.String</span></span>

### <span data-ttu-id="8d584-133">[System.object]. 清單 ' 1 [PSPrivateDnsZoneConfig，2.5.0.0，，版本 =，Culture = 中性，PublicKeyToken = null]]。）））））</span><span class="sxs-lookup"><span data-stu-id="8d584-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8d584-134">輸出</span><span class="sxs-lookup"><span data-stu-id="8d584-134">OUTPUTS</span></span>

### <span data-ttu-id="8d584-135">PSPrivateDnsZoneGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8d584-135">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="8d584-136">筆記</span><span class="sxs-lookup"><span data-stu-id="8d584-136">NOTES</span></span>

## <span data-ttu-id="8d584-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="8d584-137">RELATED LINKS</span></span>
