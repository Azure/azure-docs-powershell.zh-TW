---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/new-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeShare.md
ms.openlocfilehash: 0046c23c53afa3e5d2b01d506a8d935020f685c2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915189"
---
# <span data-ttu-id="c8533-101">New-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="c8533-101">New-AzStackEdgeShare</span></span>

## <span data-ttu-id="c8533-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c8533-102">SYNOPSIS</span></span>
<span data-ttu-id="c8533-103">在裝置上建立新共用。</span><span class="sxs-lookup"><span data-stu-id="c8533-103">Creates a new share on the device.</span></span>

## <span data-ttu-id="c8533-104">語法</span><span class="sxs-lookup"><span data-stu-id="c8533-104">SYNTAX</span></span>

### <span data-ttu-id="c8533-105">SmbParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c8533-105">SmbParameterSet (Default)</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c8533-106">CloudShareNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8533-106">CloudShareNfsParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c8533-107">CloudShareSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8533-107">CloudShareSmbParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c8533-108">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8533-108">NfsParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c8533-109">描述</span><span class="sxs-lookup"><span data-stu-id="c8533-109">DESCRIPTION</span></span>
<span data-ttu-id="c8533-110">**New-AzStackEdgeShare** Cmdlet 在 Stack Edge 裝置上建立新共用。</span><span class="sxs-lookup"><span data-stu-id="c8533-110">The **New-AzStackEdgeShare** cmdlet creates a new share on the Stack Edge device.</span></span>

## <span data-ttu-id="c8533-111">例子</span><span class="sxs-lookup"><span data-stu-id="c8533-111">EXAMPLES</span></span>

### <span data-ttu-id="c8533-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="c8533-112">Example 1</span></span>
```
PS C:\> New-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share-1 -SMB
-StorageAccountCredentialName storageCredentialName -DataFormat PageBlob
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="c8533-113">參數</span><span class="sxs-lookup"><span data-stu-id="c8533-113">PARAMETERS</span></span>

### <span data-ttu-id="c8533-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8533-114">-AsJob</span></span>
<span data-ttu-id="c8533-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c8533-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c8533-116">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="c8533-116">-ClientAccessRight</span></span>
<span data-ttu-id="c8533-117">ClientIds 的讀/寫 Access，例如：@ (@{"ClientId"="192.168.10.10";」AccessRight"="NoAccess"}， @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"}) </span><span class="sxs-lookup"><span data-stu-id="c8533-117">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

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

### <span data-ttu-id="c8533-118">-CloudShare</span><span class="sxs-lookup"><span data-stu-id="c8533-118">-CloudShare</span></span>
<span data-ttu-id="c8533-119">提供現有的 StorageAccountCredential 資源名稱</span><span class="sxs-lookup"><span data-stu-id="c8533-119">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="c8533-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="c8533-120">-ContainerName</span></span>
<span data-ttu-id="c8533-121">容器名稱 (根據指定的資料格式，這代表 Azure 檔案/Pageblob/Block blob) </span><span class="sxs-lookup"><span data-stu-id="c8533-121">Container name (Based on the data format specified, this represents the name of Azure Files/Pageblob/Block blob)</span></span>

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

### <span data-ttu-id="c8533-122">-資料格式</span><span class="sxs-lookup"><span data-stu-id="c8533-122">-DataFormat</span></span>
<span data-ttu-id="c8533-123">設定資料格式，例如：PageBlob、BlobBlob</span><span class="sxs-lookup"><span data-stu-id="c8533-123">Set Data Format ex: PageBlob, BlobBlob</span></span>

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

### <span data-ttu-id="c8533-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8533-124">-DefaultProfile</span></span>
<span data-ttu-id="c8533-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c8533-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8533-126">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="c8533-126">-DeviceName</span></span>
<span data-ttu-id="c8533-127">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="c8533-127">Device Name</span></span>

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

### <span data-ttu-id="c8533-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="c8533-128">-Name</span></span>
<span data-ttu-id="c8533-129">資源名稱</span><span class="sxs-lookup"><span data-stu-id="c8533-129">Resource Name</span></span>

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

### <span data-ttu-id="c8533-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="c8533-130">-NFS</span></span>
<span data-ttu-id="c8533-131">建立共用時，AccessProtocol</span><span class="sxs-lookup"><span data-stu-id="c8533-131">AccessProtocol in the case of creating Share</span></span>

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

### <span data-ttu-id="c8533-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8533-132">-ResourceGroupName</span></span>
<span data-ttu-id="c8533-133">資源組名</span><span class="sxs-lookup"><span data-stu-id="c8533-133">Resource Group Name</span></span>

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

### <span data-ttu-id="c8533-134">-SMB</span><span class="sxs-lookup"><span data-stu-id="c8533-134">-SMB</span></span>
<span data-ttu-id="c8533-135">建立共用時，AccessProtocol</span><span class="sxs-lookup"><span data-stu-id="c8533-135">AccessProtocol in the case of creating Share</span></span>

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

### <span data-ttu-id="c8533-136">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="c8533-136">-StorageAccountCredentialName</span></span>
<span data-ttu-id="c8533-137">提供現有的 StorageAccountCredential 資源名稱</span><span class="sxs-lookup"><span data-stu-id="c8533-137">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="c8533-138">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="c8533-138">-UserAccessRight</span></span>
<span data-ttu-id="c8533-139">提供存取權以及現有使用者名稱，以存取 SMB 共用類型，例如：@ (@{"Username"="user-name-1";"AccessRight"="Read"}， @{"Username"="user-name-2";"AccessRight"="Read"}， @{"Username"="user-name-3";"AccessRight"="Custom"}) </span><span class="sxs-lookup"><span data-stu-id="c8533-139">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

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

### <span data-ttu-id="c8533-140">-確認</span><span class="sxs-lookup"><span data-stu-id="c8533-140">-Confirm</span></span>
<span data-ttu-id="c8533-141">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c8533-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8533-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8533-142">-WhatIf</span></span>
<span data-ttu-id="c8533-143">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c8533-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8533-144">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c8533-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8533-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8533-145">CommonParameters</span></span>
<span data-ttu-id="c8533-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c8533-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8533-147">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8533-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8533-148">輸入</span><span class="sxs-lookup"><span data-stu-id="c8533-148">INPUTS</span></span>

### <span data-ttu-id="c8533-149">System.String</span><span class="sxs-lookup"><span data-stu-id="c8533-149">System.String</span></span>

## <span data-ttu-id="c8533-150">輸出</span><span class="sxs-lookup"><span data-stu-id="c8533-150">OUTPUTS</span></span>

### <span data-ttu-id="c8533-151">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="c8533-151">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="c8533-152">筆記</span><span class="sxs-lookup"><span data-stu-id="c8533-152">NOTES</span></span>

## <span data-ttu-id="c8533-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8533-153">RELATED LINKS</span></span>
