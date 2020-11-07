---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeShare.md
ms.openlocfilehash: 19dd22f15400e99f95947d97fe8c46077911de61
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795737"
---
# <span data-ttu-id="fe71e-101">New-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="fe71e-101">New-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="fe71e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe71e-102">SYNOPSIS</span></span>
<span data-ttu-id="fe71e-103">在裝置上建立新的共用。</span><span class="sxs-lookup"><span data-stu-id="fe71e-103">Creates a new share on the device.</span></span>

## <span data-ttu-id="fe71e-104">句法</span><span class="sxs-lookup"><span data-stu-id="fe71e-104">SYNTAX</span></span>

### <span data-ttu-id="fe71e-105">SmbParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fe71e-105">SmbParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe71e-106">CloudShareNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe71e-106">CloudShareNfsParameterSet</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe71e-107">CloudShareSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe71e-107">CloudShareSmbParameterSet</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe71e-108">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe71e-108">NfsParameterSet</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe71e-109">說明</span><span class="sxs-lookup"><span data-stu-id="fe71e-109">DESCRIPTION</span></span>
<span data-ttu-id="fe71e-110">**新的-AzDataBoxEdgeShare** Cmdlet 會在 [資料] 方塊邊緣裝置上建立新的共用。</span><span class="sxs-lookup"><span data-stu-id="fe71e-110">The **New-AzDataBoxEdgeShare** cmdlet creates a new share on the Data Box Edge device.</span></span>

## <span data-ttu-id="fe71e-111">示例</span><span class="sxs-lookup"><span data-stu-id="fe71e-111">EXAMPLES</span></span>

### <span data-ttu-id="fe71e-112">範例1</span><span class="sxs-lookup"><span data-stu-id="fe71e-112">Example 1</span></span>
```
PS C:\> New-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share-1 -SMB
-StorageAccountCredentialName storageCredentialName -DataFormat PageBlob
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="fe71e-113">參數</span><span class="sxs-lookup"><span data-stu-id="fe71e-113">PARAMETERS</span></span>

### <span data-ttu-id="fe71e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe71e-114">-AsJob</span></span>
<span data-ttu-id="fe71e-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fe71e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe71e-116">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="fe71e-116">-ClientAccessRight</span></span>
<span data-ttu-id="fe71e-117">ClientIds 的讀/寫存取權，例如： @ ( @ {"ClientId" = "192.168.10.10"; "AccessRight "=" NoAccess "}，@ {" ClientId "=" 192.168.10.11 ";"AccessRight "=" ReadOnly "} ) </span><span class="sxs-lookup"><span data-stu-id="fe71e-117">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

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

### <span data-ttu-id="fe71e-118">-CloudShare</span><span class="sxs-lookup"><span data-stu-id="fe71e-118">-CloudShare</span></span>
<span data-ttu-id="fe71e-119">提供現有 StorageAccountCredential 的資源名稱</span><span class="sxs-lookup"><span data-stu-id="fe71e-119">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="fe71e-120">-容器</span><span class="sxs-lookup"><span data-stu-id="fe71e-120">-ContainerName</span></span>
<span data-ttu-id="fe71e-121">容器名稱 (根據指定的資料格式，這代表 Azure Files/Pageblob/區塊 blob 的名稱) </span><span class="sxs-lookup"><span data-stu-id="fe71e-121">Container name (Based on the data format specified, this represents the name of Azure Files/Pageblob/Block blob)</span></span>

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

### <span data-ttu-id="fe71e-122">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="fe71e-122">-DataFormat</span></span>
<span data-ttu-id="fe71e-123">設定資料格式 ex： PageBlob、BlobBlob</span><span class="sxs-lookup"><span data-stu-id="fe71e-123">Set Data Format ex: PageBlob, BlobBlob</span></span>

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

### <span data-ttu-id="fe71e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe71e-124">-DefaultProfile</span></span>
<span data-ttu-id="fe71e-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fe71e-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe71e-126">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="fe71e-126">-DeviceName</span></span>
<span data-ttu-id="fe71e-127">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="fe71e-127">Device Name</span></span>

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

### <span data-ttu-id="fe71e-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="fe71e-128">-Name</span></span>
<span data-ttu-id="fe71e-129">資源名稱</span><span class="sxs-lookup"><span data-stu-id="fe71e-129">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe71e-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="fe71e-130">-NFS</span></span>
<span data-ttu-id="fe71e-131">在建立共用的情況下 AccessProtocol</span><span class="sxs-lookup"><span data-stu-id="fe71e-131">AccessProtocol in the case of creating Share</span></span>

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

### <span data-ttu-id="fe71e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe71e-132">-ResourceGroupName</span></span>
<span data-ttu-id="fe71e-133">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="fe71e-133">Resource Group Name</span></span>

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

### <span data-ttu-id="fe71e-134">-SMB</span><span class="sxs-lookup"><span data-stu-id="fe71e-134">-SMB</span></span>
<span data-ttu-id="fe71e-135">在建立共用的情況下 AccessProtocol</span><span class="sxs-lookup"><span data-stu-id="fe71e-135">AccessProtocol in the case of creating Share</span></span>

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

### <span data-ttu-id="fe71e-136">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="fe71e-136">-StorageAccountCredentialName</span></span>
<span data-ttu-id="fe71e-137">提供現有 StorageAccountCredential 的資源名稱</span><span class="sxs-lookup"><span data-stu-id="fe71e-137">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe71e-138">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="fe71e-138">-UserAccessRight</span></span>
<span data-ttu-id="fe71e-139">提供存取權與現有的使用者名稱，以存取 SMB 共用類型（針對 ex： @ ( @ {"Username" = "使用者名稱-1"; "）AccessRight "=" 讀取 "}，@ {" Username "=" 使用者-名稱-2 ";"AccessRight "=" 讀取 "}，@ {" Username "=" 使用者名稱-3 ";"AccessRight "=" 自訂 "} ) </span><span class="sxs-lookup"><span data-stu-id="fe71e-139">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

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

### <span data-ttu-id="fe71e-140">-確認</span><span class="sxs-lookup"><span data-stu-id="fe71e-140">-Confirm</span></span>
<span data-ttu-id="fe71e-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fe71e-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe71e-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe71e-142">-WhatIf</span></span>
<span data-ttu-id="fe71e-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fe71e-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fe71e-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fe71e-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe71e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe71e-145">CommonParameters</span></span>
<span data-ttu-id="fe71e-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe71e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe71e-147">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fe71e-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe71e-148">輸入</span><span class="sxs-lookup"><span data-stu-id="fe71e-148">INPUTS</span></span>

### <span data-ttu-id="fe71e-149">System.object</span><span class="sxs-lookup"><span data-stu-id="fe71e-149">System.String</span></span>

## <span data-ttu-id="fe71e-150">輸出</span><span class="sxs-lookup"><span data-stu-id="fe71e-150">OUTPUTS</span></span>

### <span data-ttu-id="fe71e-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="fe71e-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="fe71e-152">筆記</span><span class="sxs-lookup"><span data-stu-id="fe71e-152">NOTES</span></span>

## <span data-ttu-id="fe71e-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe71e-153">RELATED LINKS</span></span>
