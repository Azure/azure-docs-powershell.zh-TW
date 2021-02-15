---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackup.md
ms.openlocfilehash: 66ba63b3e350093173ae9d1badc6c717a3c682aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131439"
---
# <span data-ttu-id="5b0f3-101">New-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="5b0f3-101">New-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="5b0f3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5b0f3-102">SYNOPSIS</span></span>
<span data-ttu-id="5b0f3-103">在 (ANF) 備份] 中建立新的 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="5b0f3-103">Creates a new Azure NetApp Files (ANF) backup.</span></span>

## <span data-ttu-id="5b0f3-104">句法</span><span class="sxs-lookup"><span data-stu-id="5b0f3-104">SYNTAX</span></span>

### <span data-ttu-id="5b0f3-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5b0f3-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesBackup -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> -Label <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b0f3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b0f3-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesBackup -Name <String> -Label <String> -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b0f3-107">說明</span><span class="sxs-lookup"><span data-stu-id="5b0f3-107">DESCRIPTION</span></span>
<span data-ttu-id="5b0f3-108">**新的-AzNetAppFilesBackup** Cmdlet 會為 ANF 的磁片卷建立備份。</span><span class="sxs-lookup"><span data-stu-id="5b0f3-108">The **New-AzNetAppFilesBackup** cmdlet creates a backup for an ANF volume.</span></span>

## <span data-ttu-id="5b0f3-109">示例</span><span class="sxs-lookup"><span data-stu-id="5b0f3-109">EXAMPLES</span></span>

### <span data-ttu-id="5b0f3-110">範例1</span><span class="sxs-lookup"><span data-stu-id="5b0f3-110">Example 1</span></span>
```powershell
PS C:\> New-AzNetAppFilesBackup -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyVolumeBackup" -Label "ALabel"
```

<span data-ttu-id="5b0f3-111">這個命令會針對名為 account "MyVolume" 的卷，建立新的 ANF 備份。</span><span class="sxs-lookup"><span data-stu-id="5b0f3-111">This command creates the new ANF backup for volume named  account "MyVolume".</span></span>

## <span data-ttu-id="5b0f3-112">參數</span><span class="sxs-lookup"><span data-stu-id="5b0f3-112">PARAMETERS</span></span>

### <span data-ttu-id="5b0f3-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5b0f3-113">-AccountName</span></span>
<span data-ttu-id="5b0f3-114">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="5b0f3-114">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0f3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b0f3-115">-DefaultProfile</span></span>
<span data-ttu-id="5b0f3-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5b0f3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b0f3-117">-標籤</span><span class="sxs-lookup"><span data-stu-id="5b0f3-117">-Label</span></span>
<span data-ttu-id="5b0f3-118">備份標籤</span><span class="sxs-lookup"><span data-stu-id="5b0f3-118">Label for backup</span></span>

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

### <span data-ttu-id="5b0f3-119">-位置</span><span class="sxs-lookup"><span data-stu-id="5b0f3-119">-Location</span></span>
<span data-ttu-id="5b0f3-120">資源的位置</span><span class="sxs-lookup"><span data-stu-id="5b0f3-120">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0f3-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="5b0f3-121">-Name</span></span>
<span data-ttu-id="5b0f3-122">ANF 備份的名稱</span><span class="sxs-lookup"><span data-stu-id="5b0f3-122">The name of the ANF backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0f3-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="5b0f3-123">-PoolName</span></span>
<span data-ttu-id="5b0f3-124">ANF 池的名稱</span><span class="sxs-lookup"><span data-stu-id="5b0f3-124">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0f3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b0f3-125">-ResourceGroupName</span></span>
<span data-ttu-id="5b0f3-126">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="5b0f3-126">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0f3-127">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="5b0f3-127">-VolumeName</span></span>
<span data-ttu-id="5b0f3-128">ANF 體積的名稱</span><span class="sxs-lookup"><span data-stu-id="5b0f3-128">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0f3-129">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="5b0f3-129">-VolumeObject</span></span>
<span data-ttu-id="5b0f3-130">新備份物件的音量</span><span class="sxs-lookup"><span data-stu-id="5b0f3-130">The volume for the new backup object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b0f3-131">-確認</span><span class="sxs-lookup"><span data-stu-id="5b0f3-131">-Confirm</span></span>
<span data-ttu-id="5b0f3-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5b0f3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b0f3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b0f3-133">-WhatIf</span></span>
<span data-ttu-id="5b0f3-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5b0f3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b0f3-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5b0f3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b0f3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b0f3-136">CommonParameters</span></span>
<span data-ttu-id="5b0f3-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5b0f3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b0f3-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5b0f3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b0f3-139">輸入</span><span class="sxs-lookup"><span data-stu-id="5b0f3-139">INPUTS</span></span>

### <span data-ttu-id="5b0f3-140">PSNetAppFilesVolume 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="5b0f3-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="5b0f3-141">輸出</span><span class="sxs-lookup"><span data-stu-id="5b0f3-141">OUTPUTS</span></span>

### <span data-ttu-id="5b0f3-142">PSNetAppFilesBackup 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="5b0f3-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="5b0f3-143">筆記</span><span class="sxs-lookup"><span data-stu-id="5b0f3-143">NOTES</span></span>

## <span data-ttu-id="5b0f3-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="5b0f3-144">RELATED LINKS</span></span>
