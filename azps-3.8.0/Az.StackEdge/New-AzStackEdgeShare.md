---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeShare.md
ms.openlocfilehash: 12ab6c1948f0864c7dcb930d0a658088fd83262c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959010"
---
# <span data-ttu-id="96f51-101">New-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="96f51-101">New-AzStackEdgeShare</span></span>

## <span data-ttu-id="96f51-102">摘要</span><span class="sxs-lookup"><span data-stu-id="96f51-102">SYNOPSIS</span></span>
<span data-ttu-id="96f51-103">在裝置上建立新的共用。</span><span class="sxs-lookup"><span data-stu-id="96f51-103">Creates a new share on the device.</span></span>

## <span data-ttu-id="96f51-104">句法</span><span class="sxs-lookup"><span data-stu-id="96f51-104">SYNTAX</span></span>

### <span data-ttu-id="96f51-105">SmbParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="96f51-105">SmbParameterSet (Default)</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="96f51-106">CloudShareNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="96f51-106">CloudShareNfsParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="96f51-107">CloudShareSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="96f51-107">CloudShareSmbParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="96f51-108">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="96f51-108">NfsParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="96f51-109">說明</span><span class="sxs-lookup"><span data-stu-id="96f51-109">DESCRIPTION</span></span>
<span data-ttu-id="96f51-110">**新的-AzStackEdgeShare** Cmdlet 會在堆疊 Edge 裝置上建立新的共用。</span><span class="sxs-lookup"><span data-stu-id="96f51-110">The **New-AzStackEdgeShare** cmdlet creates a new share on the Stack Edge device.</span></span>

## <span data-ttu-id="96f51-111">示例</span><span class="sxs-lookup"><span data-stu-id="96f51-111">EXAMPLES</span></span>

### <span data-ttu-id="96f51-112">範例1</span><span class="sxs-lookup"><span data-stu-id="96f51-112">Example 1</span></span>
```
PS C:\> New-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share-1 -SMB
-StorageAccountCredentialName storageCredentialName -DataFormat PageBlob
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="96f51-113">參數</span><span class="sxs-lookup"><span data-stu-id="96f51-113">PARAMETERS</span></span>

### <span data-ttu-id="96f51-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96f51-114">-AsJob</span></span>
<span data-ttu-id="96f51-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="96f51-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="96f51-116">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="96f51-116">-ClientAccessRight</span></span>
<span data-ttu-id="96f51-117">ClientIds 的讀/寫存取權，例如： @ ( @ {"ClientId" = "192.168.10.10"; "AccessRight "=" NoAccess "}，@ {" ClientId "=" 192.168.10.11 ";"AccessRight "=" ReadOnly "} ) </span><span class="sxs-lookup"><span data-stu-id="96f51-117">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: CloudShareNfsParameterSet, NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96f51-118">-CloudShare</span><span class="sxs-lookup"><span data-stu-id="96f51-118">-CloudShare</span></span>
<span data-ttu-id="96f51-119">提供現有 StorageAccountCredential 的資源名稱</span><span class="sxs-lookup"><span data-stu-id="96f51-119">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96f51-120">-容器</span><span class="sxs-lookup"><span data-stu-id="96f51-120">-ContainerName</span></span>
<span data-ttu-id="96f51-121">容器名稱 (根據指定的資料格式，這代表 Azure Files/Pageblob/區塊 blob 的名稱) </span><span class="sxs-lookup"><span data-stu-id="96f51-121">Container name (Based on the data format specified, this represents the name of Azure Files/Pageblob/Block blob)</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96f51-122">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="96f51-122">-DataFormat</span></span>
<span data-ttu-id="96f51-123">設定資料格式 ex： PageBlob、BlobBlob</span><span class="sxs-lookup"><span data-stu-id="96f51-123">Set Data Format ex: PageBlob, BlobBlob</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96f51-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96f51-124">-DefaultProfile</span></span>
<span data-ttu-id="96f51-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="96f51-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96f51-126">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="96f51-126">-DeviceName</span></span>
<span data-ttu-id="96f51-127">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="96f51-127">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96f51-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="96f51-128">-Name</span></span>
<span data-ttu-id="96f51-129">資源名稱</span><span class="sxs-lookup"><span data-stu-id="96f51-129">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96f51-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="96f51-130">-NFS</span></span>
<span data-ttu-id="96f51-131">在建立共用的情況下 AccessProtocol</span><span class="sxs-lookup"><span data-stu-id="96f51-131">AccessProtocol in the case of creating Share</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloudShareNfsParameterSet, NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96f51-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96f51-132">-ResourceGroupName</span></span>
<span data-ttu-id="96f51-133">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="96f51-133">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96f51-134">-SMB</span><span class="sxs-lookup"><span data-stu-id="96f51-134">-SMB</span></span>
<span data-ttu-id="96f51-135">在建立共用的情況下 AccessProtocol</span><span class="sxs-lookup"><span data-stu-id="96f51-135">AccessProtocol in the case of creating Share</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SmbParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96f51-136">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="96f51-136">-StorageAccountCredentialName</span></span>
<span data-ttu-id="96f51-137">提供現有 StorageAccountCredential 的資源名稱</span><span class="sxs-lookup"><span data-stu-id="96f51-137">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96f51-138">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="96f51-138">-UserAccessRight</span></span>
<span data-ttu-id="96f51-139">提供存取權與現有的使用者名稱，以存取 SMB 共用類型（針對 ex： @ ( @ {"Username" = "使用者名稱-1"; "）AccessRight "=" 讀取 "}，@ {" Username "=" 使用者-名稱-2 ";"AccessRight "=" 讀取 "}，@ {" Username "=" 使用者名稱-3 ";"AccessRight "=" 自訂 "} ) </span><span class="sxs-lookup"><span data-stu-id="96f51-139">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: SmbParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96f51-140">-確認</span><span class="sxs-lookup"><span data-stu-id="96f51-140">-Confirm</span></span>
<span data-ttu-id="96f51-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="96f51-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96f51-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96f51-142">-WhatIf</span></span>
<span data-ttu-id="96f51-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="96f51-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96f51-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="96f51-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96f51-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96f51-145">CommonParameters</span></span>
<span data-ttu-id="96f51-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="96f51-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96f51-147">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="96f51-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96f51-148">輸入</span><span class="sxs-lookup"><span data-stu-id="96f51-148">INPUTS</span></span>

### <span data-ttu-id="96f51-149">System.object</span><span class="sxs-lookup"><span data-stu-id="96f51-149">System.String</span></span>

## <span data-ttu-id="96f51-150">輸出</span><span class="sxs-lookup"><span data-stu-id="96f51-150">OUTPUTS</span></span>

### <span data-ttu-id="96f51-151">PSStackEdgeShare （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="96f51-151">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="96f51-152">筆記</span><span class="sxs-lookup"><span data-stu-id="96f51-152">NOTES</span></span>

## <span data-ttu-id="96f51-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="96f51-153">RELATED LINKS</span></span>
