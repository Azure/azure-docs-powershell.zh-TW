---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratediskmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
ms.openlocfilehash: 812b1a3de090240a306f3d0a5b768ce25f3b22e5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288803"
---
# <span data-ttu-id="7ef88-101">New-AzMigrateDiskMapping</span><span class="sxs-lookup"><span data-stu-id="7ef88-101">New-AzMigrateDiskMapping</span></span>

## <span data-ttu-id="7ef88-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7ef88-102">SYNOPSIS</span></span>
<span data-ttu-id="7ef88-103">建立新的磁片對應</span><span class="sxs-lookup"><span data-stu-id="7ef88-103">Creates a new disk mapping</span></span>

## <span data-ttu-id="7ef88-104">句法</span><span class="sxs-lookup"><span data-stu-id="7ef88-104">SYNTAX</span></span>

```
New-AzMigrateDiskMapping -DiskID <String> -DiskType <DiskAccountType> -IsOSDisk <String>
 [-DiskEncryptionSetID <String>] [<CommonParameters>]
```

## <span data-ttu-id="7ef88-105">說明</span><span class="sxs-lookup"><span data-stu-id="7ef88-105">DESCRIPTION</span></span>
<span data-ttu-id="7ef88-106">New-AzMigrateDiskMapping Cmdlet 會建立連接至伺服器的來源磁片對應，以進行遷移</span><span class="sxs-lookup"><span data-stu-id="7ef88-106">The New-AzMigrateDiskMapping cmdlet creates a mapping of the source disk attached to the server to be migrated</span></span>

## <span data-ttu-id="7ef88-107">示例</span><span class="sxs-lookup"><span data-stu-id="7ef88-107">EXAMPLES</span></span>

### <span data-ttu-id="7ef88-108">範例1：製作磁片</span><span class="sxs-lookup"><span data-stu-id="7ef88-108">Example 1: Make disks</span></span>
```powershell
PS C:\> New-AzMigrateDiskMapping -DiskID a -DiskType Standard -IsOSDisk 'true'

DiskEncryptionSetId DiskId   DiskType  IsOSDisk LogStorageAccountId LogStorageAccountSasSecretName  
------------------- ------   --------  -------- ------------------- ------------------------------   
                      a      Standard  true  
```

<span data-ttu-id="7ef88-109">取得磁片物件以提供 New-AzMigrateServerReplication 的輸入</span><span class="sxs-lookup"><span data-stu-id="7ef88-109">Get disks object to provide input for New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="7ef88-110">參數</span><span class="sxs-lookup"><span data-stu-id="7ef88-110">PARAMETERS</span></span>

### <span data-ttu-id="7ef88-111">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="7ef88-111">-DiskEncryptionSetID</span></span>
<span data-ttu-id="7ef88-112">指定要使用的磁片 encyption 集。</span><span class="sxs-lookup"><span data-stu-id="7ef88-112">Specifies the disk encyption set to be used.</span></span>

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

### <span data-ttu-id="7ef88-113">-DiskID</span><span class="sxs-lookup"><span data-stu-id="7ef88-113">-DiskID</span></span>
<span data-ttu-id="7ef88-114">指定附加到已探索伺服器的磁片識別碼，以進行遷移。</span><span class="sxs-lookup"><span data-stu-id="7ef88-114">Specifies the disk ID of the disk attached to the discovered server to be migrated.</span></span>

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

### <span data-ttu-id="7ef88-115">-DiskType</span><span class="sxs-lookup"><span data-stu-id="7ef88-115">-DiskType</span></span>
<span data-ttu-id="7ef88-116">指定要用於 Azure VM 的磁片類型。</span><span class="sxs-lookup"><span data-stu-id="7ef88-116">Specifies the type of disks to be used for the Azure VM.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Support.DiskAccountType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ef88-117">-IsOSDisk</span><span class="sxs-lookup"><span data-stu-id="7ef88-117">-IsOSDisk</span></span>
<span data-ttu-id="7ef88-118">指定磁片是否包含要遷移之來源伺服器的作業系統。</span><span class="sxs-lookup"><span data-stu-id="7ef88-118">Specifies whether the disk contains the Operating System for the source server to be migrated.</span></span>

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

### <span data-ttu-id="7ef88-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ef88-119">CommonParameters</span></span>
<span data-ttu-id="7ef88-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7ef88-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ef88-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7ef88-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ef88-122">輸入</span><span class="sxs-lookup"><span data-stu-id="7ef88-122">INPUTS</span></span>

## <span data-ttu-id="7ef88-123">輸出</span><span class="sxs-lookup"><span data-stu-id="7ef88-123">OUTPUTS</span></span>

### <span data-ttu-id="7ef88-124">IVMwareCbtDiskInput 中的 Api20180110 （）。</span><span class="sxs-lookup"><span data-stu-id="7ef88-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span></span>

## <span data-ttu-id="7ef88-125">筆記</span><span class="sxs-lookup"><span data-stu-id="7ef88-125">NOTES</span></span>

<span data-ttu-id="7ef88-126">別名</span><span class="sxs-lookup"><span data-stu-id="7ef88-126">ALIASES</span></span>

## <span data-ttu-id="7ef88-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="7ef88-127">RELATED LINKS</span></span>

