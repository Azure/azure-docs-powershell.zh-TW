---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratenicmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
ms.openlocfilehash: 118e96747d3859a7b9132747052fb3407b7201ae
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281315"
---
# <span data-ttu-id="fe24f-101">New-AzMigrateNicMapping</span><span class="sxs-lookup"><span data-stu-id="fe24f-101">New-AzMigrateNicMapping</span></span>

## <span data-ttu-id="fe24f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe24f-102">SYNOPSIS</span></span>
<span data-ttu-id="fe24f-103">建立物件以更新複製伺服器的 NIC 屬性。</span><span class="sxs-lookup"><span data-stu-id="fe24f-103">Creates an object to update NIC properties of a replicating server.</span></span>

## <span data-ttu-id="fe24f-104">句法</span><span class="sxs-lookup"><span data-stu-id="fe24f-104">SYNTAX</span></span>

```
New-AzMigrateNicMapping -NicID <String> [-TargetNicIP <String>] [-TargetNicSelectionType <String>]
 [-TargetNicSubnet <String>] [<CommonParameters>]
```

## <span data-ttu-id="fe24f-105">說明</span><span class="sxs-lookup"><span data-stu-id="fe24f-105">DESCRIPTION</span></span>
<span data-ttu-id="fe24f-106">New-AzMigrateNicMapping Cmdlet 會建立連接至伺服器的來源 NIC 的對應，以進行遷移。</span><span class="sxs-lookup"><span data-stu-id="fe24f-106">The New-AzMigrateNicMapping cmdlet creates a mapping of the source NIC attached to the server to be migrated.</span></span>
<span data-ttu-id="fe24f-107">這個物件是以 Set-AzMigrateServerReplication Cmdlet 的輸入提供，以更新複製伺服器的 NIC 及其屬性。</span><span class="sxs-lookup"><span data-stu-id="fe24f-107">This object is provided as an input to the Set-AzMigrateServerReplication cmdlet to update the NIC and its properties for a replicating server.</span></span>

## <span data-ttu-id="fe24f-108">示例</span><span class="sxs-lookup"><span data-stu-id="fe24f-108">EXAMPLES</span></span>

### <span data-ttu-id="fe24f-109">範例1：建立 NIC 物件</span><span class="sxs-lookup"><span data-stu-id="fe24f-109">Example 1: Create a NIC object</span></span>
```powershell
PS C:\> New-AzMigrateNicMapping -NicID a2399354-653a-464e-a567-d30ef5467a31 -TargetNicSelectionType primary -TargetNicIP "172.17.1.17"

IsPrimaryNic IsSelectedForMigration NicId                                TargetStaticIPAddress TargetSubnetName
------------ ---------------------- -----                                --------------------- ----------------
false        false                  a2399354-653a-464e-a567-d30ef5467a31
```

<span data-ttu-id="fe24f-110">建立 NIC 更新物件。</span><span class="sxs-lookup"><span data-stu-id="fe24f-110">Creates a NIC update object.</span></span>

## <span data-ttu-id="fe24f-111">參數</span><span class="sxs-lookup"><span data-stu-id="fe24f-111">PARAMETERS</span></span>

### <span data-ttu-id="fe24f-112">-NicID</span><span class="sxs-lookup"><span data-stu-id="fe24f-112">-NicID</span></span>
<span data-ttu-id="fe24f-113">指定要更新之 NIC 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fe24f-113">Specifies the ID of the NIC to be updated.</span></span>

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

### <span data-ttu-id="fe24f-114">-TargetNicIP</span><span class="sxs-lookup"><span data-stu-id="fe24f-114">-TargetNicIP</span></span>
<span data-ttu-id="fe24f-115">指定要用於 NIC 的目的地子網中的 IP。</span><span class="sxs-lookup"><span data-stu-id="fe24f-115">Specifies the IP within the destination subnet to be used for the NIC.</span></span>

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

### <span data-ttu-id="fe24f-116">-TargetNicSelectionType</span><span class="sxs-lookup"><span data-stu-id="fe24f-116">-TargetNicSelectionType</span></span>
<span data-ttu-id="fe24f-117">指定要更新的 NIC 是 [主要]、[次要] 或 [未遷移]。</span><span class="sxs-lookup"><span data-stu-id="fe24f-117">Specifies whether the NIC to be updated will be the primary, secondary or not migrated.</span></span>

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

### <span data-ttu-id="fe24f-118">-TargetNicSubnet</span><span class="sxs-lookup"><span data-stu-id="fe24f-118">-TargetNicSubnet</span></span>
<span data-ttu-id="fe24f-119">指定要將伺服器遷移至其中之目標虛擬網路中之 NIC 的子網名稱。</span><span class="sxs-lookup"><span data-stu-id="fe24f-119">Specifies the Subnet name for the NIC in the destination Virtual Network to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="fe24f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe24f-120">CommonParameters</span></span>
<span data-ttu-id="fe24f-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe24f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe24f-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fe24f-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe24f-123">輸入</span><span class="sxs-lookup"><span data-stu-id="fe24f-123">INPUTS</span></span>

## <span data-ttu-id="fe24f-124">輸出</span><span class="sxs-lookup"><span data-stu-id="fe24f-124">OUTPUTS</span></span>

### <span data-ttu-id="fe24f-125">IVMwareCbtNicInput 中的 Api20180110 （）。</span><span class="sxs-lookup"><span data-stu-id="fe24f-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput</span></span>

## <span data-ttu-id="fe24f-126">筆記</span><span class="sxs-lookup"><span data-stu-id="fe24f-126">NOTES</span></span>

<span data-ttu-id="fe24f-127">別名</span><span class="sxs-lookup"><span data-stu-id="fe24f-127">ALIASES</span></span>

## <span data-ttu-id="fe24f-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe24f-128">RELATED LINKS</span></span>

