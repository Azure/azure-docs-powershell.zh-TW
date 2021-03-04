---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: fc1c3a9641134c113713dab0c53b22027f2b7280
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903489"
---
# <span data-ttu-id="4c316-101">New-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="4c316-101">New-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="4c316-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4c316-102">SYNOPSIS</span></span>
<span data-ttu-id="4c316-103">在指定的私人端點中建立私人 DNS 區域群組。</span><span class="sxs-lookup"><span data-stu-id="4c316-103">Creates a private DNS zone group in the specified private endpoint.</span></span>

## <span data-ttu-id="4c316-104">語法</span><span class="sxs-lookup"><span data-stu-id="4c316-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c316-105">描述</span><span class="sxs-lookup"><span data-stu-id="4c316-105">DESCRIPTION</span></span>
<span data-ttu-id="4c316-106">**New-AzPrivateDnsZoneGroup** Cmdlet 可讓您建立新的私人 DNS 區域群組。</span><span class="sxs-lookup"><span data-stu-id="4c316-106">The **New-AzPrivateDnsZoneGroup** cmdlet enables you to create a new private DNS zone group.</span></span>

## <span data-ttu-id="4c316-107">例子</span><span class="sxs-lookup"><span data-stu-id="4c316-107">EXAMPLES</span></span>

### <span data-ttu-id="4c316-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="4c316-108">Example 1</span></span>
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
PS C:\> New-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name "dnsgroup1" -PrivateDnsZoneConfig $config -Force
Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/test-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test.vault.azure.com",
                            "RecordSets": []
                          }
                        ]
```

<span data-ttu-id="4c316-109">建立私人端點 `test-pr-endpoint` 後，上述範例會建立該私人端點下的 DNS 區域群組。</span><span class="sxs-lookup"><span data-stu-id="4c316-109">Once private endpoint `test-pr-endpoint` is created, above example creates DNS zone group under that private endpoint.</span></span>

## <span data-ttu-id="4c316-110">參數</span><span class="sxs-lookup"><span data-stu-id="4c316-110">PARAMETERS</span></span>

### <span data-ttu-id="4c316-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c316-111">-AsJob</span></span>
<span data-ttu-id="4c316-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4c316-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4c316-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c316-113">-DefaultProfile</span></span>
<span data-ttu-id="4c316-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4c316-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c316-115">-強制</span><span class="sxs-lookup"><span data-stu-id="4c316-115">-Force</span></span>
<span data-ttu-id="4c316-116">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="4c316-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="4c316-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="4c316-117">-Name</span></span>
<span data-ttu-id="4c316-118">私人 dns 區域組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4c316-118">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="4c316-119">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="4c316-119">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="4c316-120">私人 dns 區域群組的專用 dns 區域組組集合。</span><span class="sxs-lookup"><span data-stu-id="4c316-120">A collection of private dns zone configurations of the private dns zone group.</span></span>

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

### <span data-ttu-id="4c316-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="4c316-121">-PrivateEndpointName</span></span>
<span data-ttu-id="4c316-122">私人端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="4c316-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="4c316-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c316-123">-ResourceGroupName</span></span>
<span data-ttu-id="4c316-124">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4c316-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="4c316-125">-確認</span><span class="sxs-lookup"><span data-stu-id="4c316-125">-Confirm</span></span>
<span data-ttu-id="4c316-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4c316-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c316-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c316-127">-WhatIf</span></span>
<span data-ttu-id="4c316-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4c316-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c316-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4c316-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c316-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c316-130">CommonParameters</span></span>
<span data-ttu-id="4c316-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4c316-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c316-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c316-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c316-133">輸入</span><span class="sxs-lookup"><span data-stu-id="4c316-133">INPUTS</span></span>

### <span data-ttu-id="4c316-134">System.String</span><span class="sxs-lookup"><span data-stu-id="4c316-134">System.String</span></span>

### <span data-ttu-id="4c316-135">System.Collections.generic.List'1[[Microsoft.Azure.Commands.Network.models.PSPrivateDnsZoneConfig，Microsoft.Azure.PowerShell.Cmdlets.Network，Version=2.5.0.0，Culture=neutral，PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="4c316-135">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4c316-136">輸出</span><span class="sxs-lookup"><span data-stu-id="4c316-136">OUTPUTS</span></span>

### <span data-ttu-id="4c316-137">Microsoft.Azure.Commands.Network.models.PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="4c316-137">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="4c316-138">筆記</span><span class="sxs-lookup"><span data-stu-id="4c316-138">NOTES</span></span>

## <span data-ttu-id="4c316-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="4c316-139">RELATED LINKS</span></span>
