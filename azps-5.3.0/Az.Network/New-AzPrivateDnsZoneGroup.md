---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: fff326143cf2740a085a6fcc3daa5dc89cdee646
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435750"
---
# <span data-ttu-id="d3360-101">New-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="d3360-101">New-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="d3360-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d3360-102">SYNOPSIS</span></span>
<span data-ttu-id="d3360-103">在指定的專用端點中建立專用 DNS 區域群組。</span><span class="sxs-lookup"><span data-stu-id="d3360-103">Creates a private DNS zone group in the specified private endpoint.</span></span>

## <span data-ttu-id="d3360-104">句法</span><span class="sxs-lookup"><span data-stu-id="d3360-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3360-105">說明</span><span class="sxs-lookup"><span data-stu-id="d3360-105">DESCRIPTION</span></span>
<span data-ttu-id="d3360-106">**新的-AzPrivateDnsZoneGroup** Cmdlet 可讓您建立新的專用 DNS 區域群組。</span><span class="sxs-lookup"><span data-stu-id="d3360-106">The **New-AzPrivateDnsZoneGroup** cmdlet enables you to create a new private DNS zone group.</span></span>

## <span data-ttu-id="d3360-107">示例</span><span class="sxs-lookup"><span data-stu-id="d3360-107">EXAMPLES</span></span>

### <span data-ttu-id="d3360-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d3360-108">Example 1</span></span>
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

<span data-ttu-id="d3360-109">建立私用端點之後 `test-pr-endpoint` ，上述範例會在該專用端點底下建立 DNS 區域群組。</span><span class="sxs-lookup"><span data-stu-id="d3360-109">Once private endpoint `test-pr-endpoint` is created, above example creates DNS zone group under that private endpoint.</span></span>

## <span data-ttu-id="d3360-110">參數</span><span class="sxs-lookup"><span data-stu-id="d3360-110">PARAMETERS</span></span>

### <span data-ttu-id="d3360-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3360-111">-AsJob</span></span>
<span data-ttu-id="d3360-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d3360-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3360-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3360-113">-DefaultProfile</span></span>
<span data-ttu-id="d3360-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d3360-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3360-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d3360-115">-Force</span></span>
<span data-ttu-id="d3360-116">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="d3360-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d3360-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="d3360-117">-Name</span></span>
<span data-ttu-id="d3360-118">專用 dns 區域群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d3360-118">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="d3360-119">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="d3360-119">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="d3360-120">私人 dns 區域群組的專用 dns 區域設定集合。</span><span class="sxs-lookup"><span data-stu-id="d3360-120">A collection of private dns zone configurations of the private dns zone group.</span></span>

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

### <span data-ttu-id="d3360-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="d3360-121">-PrivateEndpointName</span></span>
<span data-ttu-id="d3360-122">私人端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="d3360-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="d3360-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3360-123">-ResourceGroupName</span></span>
<span data-ttu-id="d3360-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d3360-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="d3360-125">-確認</span><span class="sxs-lookup"><span data-stu-id="d3360-125">-Confirm</span></span>
<span data-ttu-id="d3360-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d3360-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3360-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3360-127">-WhatIf</span></span>
<span data-ttu-id="d3360-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d3360-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3360-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d3360-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3360-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3360-130">CommonParameters</span></span>
<span data-ttu-id="d3360-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d3360-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3360-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d3360-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3360-133">輸入</span><span class="sxs-lookup"><span data-stu-id="d3360-133">INPUTS</span></span>

### <span data-ttu-id="d3360-134">System.object</span><span class="sxs-lookup"><span data-stu-id="d3360-134">System.String</span></span>

### <span data-ttu-id="d3360-135">[System.object]. 清單 ' 1 [PSPrivateDnsZoneConfig，2.5.0.0，，版本 =，Culture = 中性，PublicKeyToken = null]]。）））））</span><span class="sxs-lookup"><span data-stu-id="d3360-135">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d3360-136">輸出</span><span class="sxs-lookup"><span data-stu-id="d3360-136">OUTPUTS</span></span>

### <span data-ttu-id="d3360-137">PSPrivateDnsZoneGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d3360-137">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="d3360-138">筆記</span><span class="sxs-lookup"><span data-stu-id="d3360-138">NOTES</span></span>

## <span data-ttu-id="d3360-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="d3360-139">RELATED LINKS</span></span>
