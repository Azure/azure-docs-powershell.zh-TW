---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeShare.md
ms.openlocfilehash: 2b6c5d5f2295398975d912521ff6d0f001bbd3a2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134474"
---
# <span data-ttu-id="3cbb2-101">Set-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="3cbb2-101">Set-AzStackEdgeShare</span></span>

## <span data-ttu-id="3cbb2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3cbb2-102">SYNOPSIS</span></span>
<span data-ttu-id="3cbb2-103">更新裝置的共用。</span><span class="sxs-lookup"><span data-stu-id="3cbb2-103">Updates the share for a device.</span></span>

## <span data-ttu-id="3cbb2-104">句法</span><span class="sxs-lookup"><span data-stu-id="3cbb2-104">SYNTAX</span></span>

### <span data-ttu-id="3cbb2-105">SmbParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3cbb2-105">SmbParameterSet (Default)</span></span>
```
Set-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -UserAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3cbb2-106">UpdateByResourceIdSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cbb2-106">UpdateByResourceIdSmbParameterSet</span></span>
```
Set-AzStackEdgeShare -ResourceId <String> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cbb2-107">UpdateByResourceIdNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cbb2-107">UpdateByResourceIdNfsParameterSet</span></span>
```
Set-AzStackEdgeShare -ResourceId <String> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cbb2-108">UpdateByInputObjectSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cbb2-108">UpdateByInputObjectSmbParameterSet</span></span>
```
Set-AzStackEdgeShare -InputObject <PSStackEdgeShare> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cbb2-109">UpdateByInputObjectNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cbb2-109">UpdateByInputObjectNfsParameterSet</span></span>
```
Set-AzStackEdgeShare -InputObject <PSStackEdgeShare> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cbb2-110">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cbb2-110">NfsParameterSet</span></span>
```
Set-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ClientAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3cbb2-111">說明</span><span class="sxs-lookup"><span data-stu-id="3cbb2-111">DESCRIPTION</span></span>
<span data-ttu-id="3cbb2-112">這個 **AzStackEdgeShare** 會取代存取權</span><span class="sxs-lookup"><span data-stu-id="3cbb2-112">This **Set-AzStackEdgeShare** will replace the access rights</span></span>

## <span data-ttu-id="3cbb2-113">示例</span><span class="sxs-lookup"><span data-stu-id="3cbb2-113">EXAMPLES</span></span>

### <span data-ttu-id="3cbb2-114">範例1</span><span class="sxs-lookup"><span data-stu-id="3cbb2-114">Example 1</span></span>
```powershell
PS C:\> $AccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
PS C:\> Set-AzStackEdgeShare -ResourceGroupName resource-group-name -ClientAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-2    NFS        Cloud            PageBlob         resource-group-name   storage-account-name
## $ClientAccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
## Possible values for AccessRight options are 'NoAccess', 'ReadOnly', 'ReadWrite'
```

### <span data-ttu-id="3cbb2-115">範例2</span><span class="sxs-lookup"><span data-stu-id="3cbb2-115">Example 2</span></span>
```powershell
PS C:\> $AccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
PS C:\> Set-AzStackEdgeShare -ResourceGroupName resource-group-name -UserAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resource-group-name   storage-account-name
## $UserAccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
## Possible values for AccessRight are 'Change', 'Read', 'Custom'
```

## <span data-ttu-id="3cbb2-116">參數</span><span class="sxs-lookup"><span data-stu-id="3cbb2-116">PARAMETERS</span></span>

### <span data-ttu-id="3cbb2-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3cbb2-117">-AsJob</span></span>
<span data-ttu-id="3cbb2-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3cbb2-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3cbb2-119">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="3cbb2-119">-ClientAccessRight</span></span>
<span data-ttu-id="3cbb2-120">ClientIds 的讀/寫存取權，例如： @ ( @ {"ClientId" = "192.168.10.10"; "AccessRight "=" NoAccess "}，@ {" ClientId "=" 192.168.10.11 ";"AccessRight "=" ReadOnly "} ) </span><span class="sxs-lookup"><span data-stu-id="3cbb2-120">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: UpdateByResourceIdNfsParameterSet, UpdateByInputObjectNfsParameterSet, NfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cbb2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cbb2-121">-DefaultProfile</span></span>
<span data-ttu-id="3cbb2-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3cbb2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cbb2-123">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3cbb2-123">-DeviceName</span></span>
<span data-ttu-id="3cbb2-124">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="3cbb2-124">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cbb2-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3cbb2-125">-InputObject</span></span>
<span data-ttu-id="3cbb2-126">輸入物件</span><span class="sxs-lookup"><span data-stu-id="3cbb2-126">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: UpdateByInputObjectSmbParameterSet, UpdateByInputObjectNfsParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3cbb2-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="3cbb2-127">-Name</span></span>
<span data-ttu-id="3cbb2-128">資源名稱</span><span class="sxs-lookup"><span data-stu-id="3cbb2-128">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cbb2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cbb2-129">-ResourceGroupName</span></span>
<span data-ttu-id="3cbb2-130">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="3cbb2-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cbb2-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3cbb2-131">-ResourceId</span></span>
<span data-ttu-id="3cbb2-132">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="3cbb2-132">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdSmbParameterSet, UpdateByResourceIdNfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cbb2-133">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="3cbb2-133">-UserAccessRight</span></span>
<span data-ttu-id="3cbb2-134">提供存取權與現有的使用者名稱，以存取 SMB 共用類型（針對 ex： @ ( @ {"Username" = "使用者名稱-1"; "）AccessRight "=" 讀取 "}，@ {" Username "=" 使用者-名稱-2 ";"AccessRight "=" 讀取 "}，@ {" Username "=" 使用者名稱-3 ";"AccessRight "=" 自訂 "} ) </span><span class="sxs-lookup"><span data-stu-id="3cbb2-134">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: SmbParameterSet, UpdateByResourceIdSmbParameterSet, UpdateByInputObjectSmbParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cbb2-135">-確認</span><span class="sxs-lookup"><span data-stu-id="3cbb2-135">-Confirm</span></span>
<span data-ttu-id="3cbb2-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3cbb2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cbb2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cbb2-137">-WhatIf</span></span>
<span data-ttu-id="3cbb2-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3cbb2-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3cbb2-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3cbb2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cbb2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cbb2-140">CommonParameters</span></span>
<span data-ttu-id="3cbb2-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3cbb2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cbb2-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3cbb2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cbb2-143">輸入</span><span class="sxs-lookup"><span data-stu-id="3cbb2-143">INPUTS</span></span>

### <span data-ttu-id="3cbb2-144">System.object</span><span class="sxs-lookup"><span data-stu-id="3cbb2-144">System.String</span></span>

### <span data-ttu-id="3cbb2-145">PSStackEdgeShare （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="3cbb2-145">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="3cbb2-146">輸出</span><span class="sxs-lookup"><span data-stu-id="3cbb2-146">OUTPUTS</span></span>

### <span data-ttu-id="3cbb2-147">PSStackEdgeShare （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="3cbb2-147">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="3cbb2-148">筆記</span><span class="sxs-lookup"><span data-stu-id="3cbb2-148">NOTES</span></span>

## <span data-ttu-id="3cbb2-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="3cbb2-149">RELATED LINKS</span></span>
