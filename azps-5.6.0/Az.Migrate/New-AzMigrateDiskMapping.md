---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/new-azmigratediskmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
ms.openlocfilehash: 1fc58ff016c41e693c059ce792a8dc8aa06e0d11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909617"
---
# <span data-ttu-id="96fb3-101">New-AzMigrateDiskMapping</span><span class="sxs-lookup"><span data-stu-id="96fb3-101">New-AzMigrateDiskMapping</span></span>

## <span data-ttu-id="96fb3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="96fb3-102">SYNOPSIS</span></span>
<span data-ttu-id="96fb3-103">建立新的磁片地圖</span><span class="sxs-lookup"><span data-stu-id="96fb3-103">Creates a new disk mapping</span></span>

## <span data-ttu-id="96fb3-104">語法</span><span class="sxs-lookup"><span data-stu-id="96fb3-104">SYNTAX</span></span>

```
New-AzMigrateDiskMapping -DiskID <String> -DiskType <String> -IsOSDisk <String>
 [-DiskEncryptionSetID <String>] [<CommonParameters>]
```

## <span data-ttu-id="96fb3-105">描述</span><span class="sxs-lookup"><span data-stu-id="96fb3-105">DESCRIPTION</span></span>
<span data-ttu-id="96fb3-106">Cmdlet New-AzMigrateDiskMapping會建立連接到要移轉之伺服器之來源磁片的映射</span><span class="sxs-lookup"><span data-stu-id="96fb3-106">The New-AzMigrateDiskMapping cmdlet creates a mapping of the source disk attached to the server to be migrated</span></span>

## <span data-ttu-id="96fb3-107">例子</span><span class="sxs-lookup"><span data-stu-id="96fb3-107">EXAMPLES</span></span>

### <span data-ttu-id="96fb3-108">範例 1：製作磁片</span><span class="sxs-lookup"><span data-stu-id="96fb3-108">Example 1: Make disks</span></span>
```powershell
PS C:\> New-AzMigrateDiskMapping -DiskID a -DiskType Standard -IsOSDisk 'true'

DiskEncryptionSetId DiskId   DiskType  IsOSDisk LogStorageAccountId LogStorageAccountSasSecretName  
------------------- ------   --------  -------- ------------------- ------------------------------   
                      a      Standard  true  
```

<span data-ttu-id="96fb3-109">取得物件物件以提供資料New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="96fb3-109">Get disks object to provide input for New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="96fb3-110">參數</span><span class="sxs-lookup"><span data-stu-id="96fb3-110">PARAMETERS</span></span>

### <span data-ttu-id="96fb3-111">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="96fb3-111">-DiskEncryptionSetID</span></span>
<span data-ttu-id="96fb3-112">指定要使用的磁片 encyption 集。</span><span class="sxs-lookup"><span data-stu-id="96fb3-112">Specifies the disk encyption set to be used.</span></span>

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

### <span data-ttu-id="96fb3-113">-DiskID</span><span class="sxs-lookup"><span data-stu-id="96fb3-113">-DiskID</span></span>
<span data-ttu-id="96fb3-114">指定要移移所發現伺服器之磁片的磁片識別碼。</span><span class="sxs-lookup"><span data-stu-id="96fb3-114">Specifies the disk ID of the disk attached to the discovered server to be migrated.</span></span>

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

### <span data-ttu-id="96fb3-115">-DiskType</span><span class="sxs-lookup"><span data-stu-id="96fb3-115">-DiskType</span></span>
<span data-ttu-id="96fb3-116">指定 Azure VM 使用的磁片類型。</span><span class="sxs-lookup"><span data-stu-id="96fb3-116">Specifies the type of disks to be used for the Azure VM.</span></span>

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

### <span data-ttu-id="96fb3-117">-IsOS至上</span><span class="sxs-lookup"><span data-stu-id="96fb3-117">-IsOSDisk</span></span>
<span data-ttu-id="96fb3-118">指定磁片是否包含要移移來源伺服器的作業系統。</span><span class="sxs-lookup"><span data-stu-id="96fb3-118">Specifies whether the disk contains the Operating System for the source server to be migrated.</span></span>

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

### <span data-ttu-id="96fb3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96fb3-119">CommonParameters</span></span>
<span data-ttu-id="96fb3-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="96fb3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96fb3-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96fb3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96fb3-122">輸入</span><span class="sxs-lookup"><span data-stu-id="96fb3-122">INPUTS</span></span>

## <span data-ttu-id="96fb3-123">輸出</span><span class="sxs-lookup"><span data-stu-id="96fb3-123">OUTPUTS</span></span>

### <span data-ttu-id="96fb3-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IV疑雲圖</span><span class="sxs-lookup"><span data-stu-id="96fb3-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span></span>

## <span data-ttu-id="96fb3-125">筆記</span><span class="sxs-lookup"><span data-stu-id="96fb3-125">NOTES</span></span>

<span data-ttu-id="96fb3-126">別名</span><span class="sxs-lookup"><span data-stu-id="96fb3-126">ALIASES</span></span>

## <span data-ttu-id="96fb3-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="96fb3-127">RELATED LINKS</span></span>

