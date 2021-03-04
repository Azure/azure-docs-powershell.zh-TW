---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
ms.openlocfilehash: 8a4183c148eda0f5f560d24c2b5874ff5577e85e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906081"
---
# <span data-ttu-id="f85f0-101">Get-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="f85f0-101">Get-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="f85f0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f85f0-102">SYNOPSIS</span></span>
<span data-ttu-id="f85f0-103">在 ANF 備份中 (Azure NetApp 檔案) 詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f85f0-103">Gets details of an Azure NetApp Files (ANF) Backup.</span></span>

## <span data-ttu-id="f85f0-104">語法</span><span class="sxs-lookup"><span data-stu-id="f85f0-104">SYNTAX</span></span>

### <span data-ttu-id="f85f0-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f85f0-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesBackup -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 [-VolumeName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f85f0-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f85f0-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f85f0-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f85f0-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f85f0-108">描述</span><span class="sxs-lookup"><span data-stu-id="f85f0-108">DESCRIPTION</span></span>
<span data-ttu-id="f85f0-109">**Get-AzNetAppFilesBackup** Cmdlet 會取得 ANF 備份的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="f85f0-109">The **Get-AzNetAppFilesBackup** cmdlet gets details of an ANF backup.</span></span>

## <span data-ttu-id="f85f0-110">例子</span><span class="sxs-lookup"><span data-stu-id="f85f0-110">EXAMPLES</span></span>

### <span data-ttu-id="f85f0-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="f85f0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyBackup"
```

<span data-ttu-id="f85f0-112">此命令會從名為「MyVolume」的卷起，獲得名為「MyAnfAccount」的備份。</span><span class="sxs-lookup"><span data-stu-id="f85f0-112">This command gets the backcup named "MyAnfAccount" from the volume named "MyVolume".</span></span>

## <span data-ttu-id="f85f0-113">參數</span><span class="sxs-lookup"><span data-stu-id="f85f0-113">PARAMETERS</span></span>

### <span data-ttu-id="f85f0-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f85f0-114">-AccountName</span></span>
<span data-ttu-id="f85f0-115">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="f85f0-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="f85f0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f85f0-116">-DefaultProfile</span></span>
<span data-ttu-id="f85f0-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f85f0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f85f0-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="f85f0-118">-Name</span></span>
<span data-ttu-id="f85f0-119">ANF 備份的名稱</span><span class="sxs-lookup"><span data-stu-id="f85f0-119">The name of the ANF backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85f0-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="f85f0-120">-PoolName</span></span>
<span data-ttu-id="f85f0-121">ANF 組名</span><span class="sxs-lookup"><span data-stu-id="f85f0-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="f85f0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f85f0-122">-ResourceGroupName</span></span>
<span data-ttu-id="f85f0-123">ANF 帳戶的資源群組</span><span class="sxs-lookup"><span data-stu-id="f85f0-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="f85f0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f85f0-124">-ResourceId</span></span>
<span data-ttu-id="f85f0-125">ANF 備份的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="f85f0-125">The resource id of the ANF Backup</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f85f0-126">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="f85f0-126">-VolumeName</span></span>
<span data-ttu-id="f85f0-127">ANF 音量的名稱</span><span class="sxs-lookup"><span data-stu-id="f85f0-127">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85f0-128">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="f85f0-128">-VolumeObject</span></span>
<span data-ttu-id="f85f0-129">包含要返回之備份的音量物件</span><span class="sxs-lookup"><span data-stu-id="f85f0-129">The volume object containing the backup to return</span></span>

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

### <span data-ttu-id="f85f0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f85f0-130">CommonParameters</span></span>
<span data-ttu-id="f85f0-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f85f0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f85f0-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f85f0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f85f0-133">輸入</span><span class="sxs-lookup"><span data-stu-id="f85f0-133">INPUTS</span></span>

### <span data-ttu-id="f85f0-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f85f0-134">System.String</span></span>

### <span data-ttu-id="f85f0-135">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="f85f0-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="f85f0-136">輸出</span><span class="sxs-lookup"><span data-stu-id="f85f0-136">OUTPUTS</span></span>

### <span data-ttu-id="f85f0-137">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="f85f0-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="f85f0-138">筆記</span><span class="sxs-lookup"><span data-stu-id="f85f0-138">NOTES</span></span>

## <span data-ttu-id="f85f0-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="f85f0-139">RELATED LINKS</span></span>
