---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/new-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackup.md
ms.openlocfilehash: 6b4527430fa74efa09aa07fd120d0acf8de0edfd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906042"
---
# <span data-ttu-id="884fc-101">New-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="884fc-101">New-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="884fc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="884fc-102">SYNOPSIS</span></span>
<span data-ttu-id="884fc-103">在 ANF 備份中 (Azure NetApp) 檔案。</span><span class="sxs-lookup"><span data-stu-id="884fc-103">Creates a new Azure NetApp Files (ANF) backup.</span></span>

## <span data-ttu-id="884fc-104">語法</span><span class="sxs-lookup"><span data-stu-id="884fc-104">SYNTAX</span></span>

### <span data-ttu-id="884fc-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="884fc-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesBackup -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> -Label <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="884fc-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="884fc-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesBackup -Name <String> -Label <String> -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="884fc-107">描述</span><span class="sxs-lookup"><span data-stu-id="884fc-107">DESCRIPTION</span></span>
<span data-ttu-id="884fc-108">**New-AzNetAppFilesBackup** Cmdlet 會建立 ANF 音量的備份。</span><span class="sxs-lookup"><span data-stu-id="884fc-108">The **New-AzNetAppFilesBackup** cmdlet creates a backup for an ANF volume.</span></span>

## <span data-ttu-id="884fc-109">例子</span><span class="sxs-lookup"><span data-stu-id="884fc-109">EXAMPLES</span></span>

### <span data-ttu-id="884fc-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="884fc-110">Example 1</span></span>
```powershell
PS C:\> New-AzNetAppFilesBackup -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyVolumeBackup" -Label "ALabel"
```

<span data-ttu-id="884fc-111">此命令會針對名為「MyVolume」的大量帳戶建立新的 ANF 備份。</span><span class="sxs-lookup"><span data-stu-id="884fc-111">This command creates the new ANF backup for volume named  account "MyVolume".</span></span>

## <span data-ttu-id="884fc-112">參數</span><span class="sxs-lookup"><span data-stu-id="884fc-112">PARAMETERS</span></span>

### <span data-ttu-id="884fc-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="884fc-113">-AccountName</span></span>
<span data-ttu-id="884fc-114">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="884fc-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="884fc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="884fc-115">-DefaultProfile</span></span>
<span data-ttu-id="884fc-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="884fc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="884fc-117">-標籤</span><span class="sxs-lookup"><span data-stu-id="884fc-117">-Label</span></span>
<span data-ttu-id="884fc-118">備份標籤</span><span class="sxs-lookup"><span data-stu-id="884fc-118">Label for backup</span></span>

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

### <span data-ttu-id="884fc-119">-位置</span><span class="sxs-lookup"><span data-stu-id="884fc-119">-Location</span></span>
<span data-ttu-id="884fc-120">資源的位置</span><span class="sxs-lookup"><span data-stu-id="884fc-120">The location of the resource</span></span>

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

### <span data-ttu-id="884fc-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="884fc-121">-Name</span></span>
<span data-ttu-id="884fc-122">ANF 備份的名稱</span><span class="sxs-lookup"><span data-stu-id="884fc-122">The name of the ANF backup</span></span>

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

### <span data-ttu-id="884fc-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="884fc-123">-PoolName</span></span>
<span data-ttu-id="884fc-124">ANF 組名</span><span class="sxs-lookup"><span data-stu-id="884fc-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="884fc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="884fc-125">-ResourceGroupName</span></span>
<span data-ttu-id="884fc-126">ANF 帳戶的資源群組</span><span class="sxs-lookup"><span data-stu-id="884fc-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="884fc-127">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="884fc-127">-VolumeName</span></span>
<span data-ttu-id="884fc-128">ANF 音量的名稱</span><span class="sxs-lookup"><span data-stu-id="884fc-128">The name of the ANF volume</span></span>

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

### <span data-ttu-id="884fc-129">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="884fc-129">-VolumeObject</span></span>
<span data-ttu-id="884fc-130">新備份物件的音量</span><span class="sxs-lookup"><span data-stu-id="884fc-130">The volume for the new backup object</span></span>

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

### <span data-ttu-id="884fc-131">-確認</span><span class="sxs-lookup"><span data-stu-id="884fc-131">-Confirm</span></span>
<span data-ttu-id="884fc-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="884fc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="884fc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="884fc-133">-WhatIf</span></span>
<span data-ttu-id="884fc-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="884fc-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="884fc-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="884fc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="884fc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="884fc-136">CommonParameters</span></span>
<span data-ttu-id="884fc-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="884fc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="884fc-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="884fc-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="884fc-139">輸入</span><span class="sxs-lookup"><span data-stu-id="884fc-139">INPUTS</span></span>

### <span data-ttu-id="884fc-140">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="884fc-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="884fc-141">輸出</span><span class="sxs-lookup"><span data-stu-id="884fc-141">OUTPUTS</span></span>

### <span data-ttu-id="884fc-142">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="884fc-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="884fc-143">筆記</span><span class="sxs-lookup"><span data-stu-id="884fc-143">NOTES</span></span>

## <span data-ttu-id="884fc-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="884fc-144">RELATED LINKS</span></span>
