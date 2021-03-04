---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/set-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeShare.md
ms.openlocfilehash: 8c31f5f97b723db63253165e21d2abea220f18d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906745"
---
# <span data-ttu-id="43e76-101">Set-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="43e76-101">Set-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="43e76-102">簡介</span><span class="sxs-lookup"><span data-stu-id="43e76-102">SYNOPSIS</span></span>
<span data-ttu-id="43e76-103">更新裝置共用。</span><span class="sxs-lookup"><span data-stu-id="43e76-103">Updates the share for a device.</span></span>

## <span data-ttu-id="43e76-104">語法</span><span class="sxs-lookup"><span data-stu-id="43e76-104">SYNTAX</span></span>

### <span data-ttu-id="43e76-105">SmbParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="43e76-105">SmbParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -UserAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43e76-106">UpdateByResourceIdSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="43e76-106">UpdateByResourceIdSmbParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -ResourceId <String> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43e76-107">UpdateByResourceIdNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="43e76-107">UpdateByResourceIdNfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -ResourceId <String> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43e76-108">UpdateByInputObjectSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="43e76-108">UpdateByInputObjectSmbParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -InputObject <PSDataBoxEdgeShare> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43e76-109">UpdateByInputObjectNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="43e76-109">UpdateByInputObjectNfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -InputObject <PSDataBoxEdgeShare> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43e76-110">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="43e76-110">NfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ClientAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="43e76-111">描述</span><span class="sxs-lookup"><span data-stu-id="43e76-111">DESCRIPTION</span></span>
<span data-ttu-id="43e76-112">此 **Set-AzDataBoxEdgeShare** 將會取代存取權限</span><span class="sxs-lookup"><span data-stu-id="43e76-112">This **Set-AzDataBoxEdgeShare** will replace the access rights</span></span>

## <span data-ttu-id="43e76-113">例子</span><span class="sxs-lookup"><span data-stu-id="43e76-113">EXAMPLES</span></span>

### <span data-ttu-id="43e76-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="43e76-114">Example 1</span></span>
```powershell
PS C:\> $AccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
PS C:\> Set-AzDataBoxEdgeShare -ResourceGroupName resource-group-name -ClientAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-2    NFS        Cloud            PageBlob         resource-group-name   storage-account-name
## $ClientAccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
## Possible values for AccessRight options are 'NoAccess', 'ReadOnly', 'ReadWrite'
```

### <span data-ttu-id="43e76-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="43e76-115">Example 2</span></span>
```powershell
PS C:\> $AccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
PS C:\> Set-AzDataBoxEdgeShare -ResourceGroupName resource-group-name -UserAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resource-group-name   storage-account-name
## $UserAccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
## Possible values for AccessRight are 'Change', 'Read', 'Custom'
```

## <span data-ttu-id="43e76-116">參數</span><span class="sxs-lookup"><span data-stu-id="43e76-116">PARAMETERS</span></span>

### <span data-ttu-id="43e76-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43e76-117">-AsJob</span></span>
<span data-ttu-id="43e76-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="43e76-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43e76-119">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="43e76-119">-ClientAccessRight</span></span>
<span data-ttu-id="43e76-120">ClientIds 的讀/寫 Access，例如：@ (@{"ClientId"="192.168.10.10";」AccessRight"="NoAccess"}， @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"}) </span><span class="sxs-lookup"><span data-stu-id="43e76-120">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

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

### <span data-ttu-id="43e76-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43e76-121">-DefaultProfile</span></span>
<span data-ttu-id="43e76-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="43e76-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43e76-123">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="43e76-123">-DeviceName</span></span>
<span data-ttu-id="43e76-124">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="43e76-124">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e76-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43e76-125">-InputObject</span></span>
<span data-ttu-id="43e76-126">輸入物件</span><span class="sxs-lookup"><span data-stu-id="43e76-126">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare
Parameter Sets: UpdateByInputObjectSmbParameterSet, UpdateByInputObjectNfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43e76-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="43e76-127">-Name</span></span>
<span data-ttu-id="43e76-128">資源名稱</span><span class="sxs-lookup"><span data-stu-id="43e76-128">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e76-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43e76-129">-ResourceGroupName</span></span>
<span data-ttu-id="43e76-130">資源組名</span><span class="sxs-lookup"><span data-stu-id="43e76-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e76-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43e76-131">-ResourceId</span></span>
<span data-ttu-id="43e76-132">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="43e76-132">Azure ResourceId</span></span>

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

### <span data-ttu-id="43e76-133">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="43e76-133">-UserAccessRight</span></span>
<span data-ttu-id="43e76-134">提供存取權以及現有使用者名稱，以存取 SMB 共用類型，例如：@ (@{"Username"="user-name-1";"AccessRight"="Read"}， @{"Username"="user-name-2";"AccessRight"="Read"}， @{"Username"="user-name-3";"AccessRight"="Custom"}) </span><span class="sxs-lookup"><span data-stu-id="43e76-134">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

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

### <span data-ttu-id="43e76-135">-確認</span><span class="sxs-lookup"><span data-stu-id="43e76-135">-Confirm</span></span>
<span data-ttu-id="43e76-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="43e76-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43e76-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43e76-137">-WhatIf</span></span>
<span data-ttu-id="43e76-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="43e76-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43e76-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="43e76-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43e76-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43e76-140">CommonParameters</span></span>
<span data-ttu-id="43e76-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="43e76-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43e76-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43e76-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43e76-143">輸入</span><span class="sxs-lookup"><span data-stu-id="43e76-143">INPUTS</span></span>

### <span data-ttu-id="43e76-144">System.String</span><span class="sxs-lookup"><span data-stu-id="43e76-144">System.String</span></span>

### <span data-ttu-id="43e76-145">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="43e76-145">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="43e76-146">輸出</span><span class="sxs-lookup"><span data-stu-id="43e76-146">OUTPUTS</span></span>

### <span data-ttu-id="43e76-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="43e76-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="43e76-148">筆記</span><span class="sxs-lookup"><span data-stu-id="43e76-148">NOTES</span></span>

## <span data-ttu-id="43e76-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="43e76-149">RELATED LINKS</span></span>
