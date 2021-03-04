---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/new-azmigratenicmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
ms.openlocfilehash: 9ec976cae2afc5070303404616b3615fe54e7b81
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909613"
---
# <span data-ttu-id="7d43e-101">New-AzMigrateNicMapping</span><span class="sxs-lookup"><span data-stu-id="7d43e-101">New-AzMigrateNicMapping</span></span>

## <span data-ttu-id="7d43e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7d43e-102">SYNOPSIS</span></span>
<span data-ttu-id="7d43e-103">建立物件以更新複製伺服器的 NIC 屬性。</span><span class="sxs-lookup"><span data-stu-id="7d43e-103">Creates an object to update NIC properties of a replicating server.</span></span>

## <span data-ttu-id="7d43e-104">語法</span><span class="sxs-lookup"><span data-stu-id="7d43e-104">SYNTAX</span></span>

```
New-AzMigrateNicMapping -NicID <String> [-TargetNicIP <String>] [-TargetNicSelectionType <String>]
 [-TargetNicSubnet <String>] [<CommonParameters>]
```

## <span data-ttu-id="7d43e-105">描述</span><span class="sxs-lookup"><span data-stu-id="7d43e-105">DESCRIPTION</span></span>
<span data-ttu-id="7d43e-106">此New-AzMigrateNicMapping Cmdlet 會建立附加至要移轉之伺服器之來源 NIC 的映射。</span><span class="sxs-lookup"><span data-stu-id="7d43e-106">The New-AzMigrateNicMapping cmdlet creates a mapping of the source NIC attached to the server to be migrated.</span></span>
<span data-ttu-id="7d43e-107">此物件會提供做為 Set-AzMigrateServerReplication Cmdlet 的輸入，以更新 NIC 及其複製伺服器的屬性。</span><span class="sxs-lookup"><span data-stu-id="7d43e-107">This object is provided as an input to the Set-AzMigrateServerReplication cmdlet to update the NIC and its properties for a replicating server.</span></span>

## <span data-ttu-id="7d43e-108">例子</span><span class="sxs-lookup"><span data-stu-id="7d43e-108">EXAMPLES</span></span>

### <span data-ttu-id="7d43e-109">範例 1：建立 NIC 物件</span><span class="sxs-lookup"><span data-stu-id="7d43e-109">Example 1: Create a NIC object</span></span>
```powershell
PS C:\> New-AzMigrateNicMapping -NicID a2399354-653a-464e-a567-d30ef5467a31 -TargetNicSelectionType primary -TargetNicIP "172.17.1.17"

IsPrimaryNic IsSelectedForMigration NicId                                TargetStaticIPAddress TargetSubnetName
------------ ---------------------- -----                                --------------------- ----------------
false        false                  a2399354-653a-464e-a567-d30ef5467a31
```

<span data-ttu-id="7d43e-110">建立 NIC 更新物件。</span><span class="sxs-lookup"><span data-stu-id="7d43e-110">Creates a NIC update object.</span></span>

## <span data-ttu-id="7d43e-111">參數</span><span class="sxs-lookup"><span data-stu-id="7d43e-111">PARAMETERS</span></span>

### <span data-ttu-id="7d43e-112">-NicID</span><span class="sxs-lookup"><span data-stu-id="7d43e-112">-NicID</span></span>
<span data-ttu-id="7d43e-113">指定要更新的 NIC 識別碼。</span><span class="sxs-lookup"><span data-stu-id="7d43e-113">Specifies the ID of the NIC to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d43e-114">-TargetNicIP</span><span class="sxs-lookup"><span data-stu-id="7d43e-114">-TargetNicIP</span></span>
<span data-ttu-id="7d43e-115">指定目的地子網內要用於 NIC 的 IP。</span><span class="sxs-lookup"><span data-stu-id="7d43e-115">Specifies the IP within the destination subnet to be used for the NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d43e-116">-TargetNicSelectionType</span><span class="sxs-lookup"><span data-stu-id="7d43e-116">-TargetNicSelectionType</span></span>
<span data-ttu-id="7d43e-117">指定要更新的 NIC 是否會是主要、次要或未移移。</span><span class="sxs-lookup"><span data-stu-id="7d43e-117">Specifies whether the NIC to be updated will be the primary, secondary or not migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d43e-118">-TargetNicSubnet</span><span class="sxs-lookup"><span data-stu-id="7d43e-118">-TargetNicSubnet</span></span>
<span data-ttu-id="7d43e-119">指定伺服器需要移移的目標虛擬網路中 NIC 的子網名稱。</span><span class="sxs-lookup"><span data-stu-id="7d43e-119">Specifies the Subnet name for the NIC in the destination Virtual Network to which the server needs to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d43e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d43e-120">CommonParameters</span></span>
<span data-ttu-id="7d43e-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7d43e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d43e-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d43e-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d43e-123">輸入</span><span class="sxs-lookup"><span data-stu-id="7d43e-123">INPUTS</span></span>

## <span data-ttu-id="7d43e-124">輸出</span><span class="sxs-lookup"><span data-stu-id="7d43e-124">OUTPUTS</span></span>

### <span data-ttu-id="7d43e-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVCbtNicInput</span><span class="sxs-lookup"><span data-stu-id="7d43e-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput</span></span>

## <span data-ttu-id="7d43e-126">筆記</span><span class="sxs-lookup"><span data-stu-id="7d43e-126">NOTES</span></span>

<span data-ttu-id="7d43e-127">別名</span><span class="sxs-lookup"><span data-stu-id="7d43e-127">ALIASES</span></span>

## <span data-ttu-id="7d43e-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d43e-128">RELATED LINKS</span></span>

