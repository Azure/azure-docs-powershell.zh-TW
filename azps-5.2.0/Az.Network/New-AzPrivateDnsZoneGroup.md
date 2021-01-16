---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: fff326143cf2740a085a6fcc3daa5dc89cdee646
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275472"
---
# <span data-ttu-id="1fd79-101">New-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="1fd79-101">New-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="1fd79-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1fd79-102">SYNOPSIS</span></span>
<span data-ttu-id="1fd79-103">在指定的專用端點中建立專用 DNS 區域群組。</span><span class="sxs-lookup"><span data-stu-id="1fd79-103">Creates a private DNS zone group in the specified private endpoint.</span></span>

## <span data-ttu-id="1fd79-104">句法</span><span class="sxs-lookup"><span data-stu-id="1fd79-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fd79-105">說明</span><span class="sxs-lookup"><span data-stu-id="1fd79-105">DESCRIPTION</span></span>
<span data-ttu-id="1fd79-106">**新的-AzPrivateDnsZoneGroup** Cmdlet 可讓您建立新的專用 DNS 區域群組。</span><span class="sxs-lookup"><span data-stu-id="1fd79-106">The **New-AzPrivateDnsZoneGroup** cmdlet enables you to create a new private DNS zone group.</span></span>

## <span data-ttu-id="1fd79-107">示例</span><span class="sxs-lookup"><span data-stu-id="1fd79-107">EXAMPLES</span></span>

### <span data-ttu-id="1fd79-108">範例1</span><span class="sxs-lookup"><span data-stu-id="1fd79-108">Example 1</span></span>
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

<span data-ttu-id="1fd79-109">建立私用端點之後 `test-pr-endpoint` ，上述範例會在該專用端點底下建立 DNS 區域群組。</span><span class="sxs-lookup"><span data-stu-id="1fd79-109">Once private endpoint `test-pr-endpoint` is created, above example creates DNS zone group under that private endpoint.</span></span>

## <span data-ttu-id="1fd79-110">參數</span><span class="sxs-lookup"><span data-stu-id="1fd79-110">PARAMETERS</span></span>

### <span data-ttu-id="1fd79-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1fd79-111">-AsJob</span></span>
<span data-ttu-id="1fd79-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1fd79-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1fd79-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fd79-113">-DefaultProfile</span></span>
<span data-ttu-id="1fd79-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1fd79-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fd79-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1fd79-115">-Force</span></span>
<span data-ttu-id="1fd79-116">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="1fd79-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="1fd79-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="1fd79-117">-Name</span></span>
<span data-ttu-id="1fd79-118">專用 dns 區域群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1fd79-118">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="1fd79-119">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="1fd79-119">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="1fd79-120">私人 dns 區域群組的專用 dns 區域設定集合。</span><span class="sxs-lookup"><span data-stu-id="1fd79-120">A collection of private dns zone configurations of the private dns zone group.</span></span>

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

### <span data-ttu-id="1fd79-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="1fd79-121">-PrivateEndpointName</span></span>
<span data-ttu-id="1fd79-122">私人端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="1fd79-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="1fd79-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fd79-123">-ResourceGroupName</span></span>
<span data-ttu-id="1fd79-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1fd79-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="1fd79-125">-確認</span><span class="sxs-lookup"><span data-stu-id="1fd79-125">-Confirm</span></span>
<span data-ttu-id="1fd79-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1fd79-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fd79-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fd79-127">-WhatIf</span></span>
<span data-ttu-id="1fd79-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1fd79-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fd79-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1fd79-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fd79-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fd79-130">CommonParameters</span></span>
<span data-ttu-id="1fd79-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1fd79-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fd79-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1fd79-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fd79-133">輸入</span><span class="sxs-lookup"><span data-stu-id="1fd79-133">INPUTS</span></span>

### <span data-ttu-id="1fd79-134">System.object</span><span class="sxs-lookup"><span data-stu-id="1fd79-134">System.String</span></span>

### <span data-ttu-id="1fd79-135">[System.object]. 清單 ' 1 [PSPrivateDnsZoneConfig，2.5.0.0，，版本 =，Culture = 中性，PublicKeyToken = null]]。）））））</span><span class="sxs-lookup"><span data-stu-id="1fd79-135">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="1fd79-136">輸出</span><span class="sxs-lookup"><span data-stu-id="1fd79-136">OUTPUTS</span></span>

### <span data-ttu-id="1fd79-137">PSPrivateDnsZoneGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1fd79-137">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="1fd79-138">筆記</span><span class="sxs-lookup"><span data-stu-id="1fd79-138">NOTES</span></span>

## <span data-ttu-id="1fd79-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="1fd79-139">RELATED LINKS</span></span>
