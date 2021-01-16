---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratediskmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
ms.openlocfilehash: 812b1a3de090240a306f3d0a5b768ce25f3b22e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281316"
---
# <span data-ttu-id="8b064-101">New-AzMigrateDiskMapping</span><span class="sxs-lookup"><span data-stu-id="8b064-101">New-AzMigrateDiskMapping</span></span>

## <span data-ttu-id="8b064-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8b064-102">SYNOPSIS</span></span>
<span data-ttu-id="8b064-103">建立新的磁片對應</span><span class="sxs-lookup"><span data-stu-id="8b064-103">Creates a new disk mapping</span></span>

## <span data-ttu-id="8b064-104">句法</span><span class="sxs-lookup"><span data-stu-id="8b064-104">SYNTAX</span></span>

```
New-AzMigrateDiskMapping -DiskID <String> -DiskType <DiskAccountType> -IsOSDisk <String>
 [-DiskEncryptionSetID <String>] [<CommonParameters>]
```

## <span data-ttu-id="8b064-105">說明</span><span class="sxs-lookup"><span data-stu-id="8b064-105">DESCRIPTION</span></span>
<span data-ttu-id="8b064-106">New-AzMigrateDiskMapping Cmdlet 會建立連接至伺服器的來源磁片對應，以進行遷移</span><span class="sxs-lookup"><span data-stu-id="8b064-106">The New-AzMigrateDiskMapping cmdlet creates a mapping of the source disk attached to the server to be migrated</span></span>

## <span data-ttu-id="8b064-107">示例</span><span class="sxs-lookup"><span data-stu-id="8b064-107">EXAMPLES</span></span>

### <span data-ttu-id="8b064-108">範例1：製作磁片</span><span class="sxs-lookup"><span data-stu-id="8b064-108">Example 1: Make disks</span></span>
```powershell
PS C:\> New-AzMigrateDiskMapping -DiskID a -DiskType Standard -IsOSDisk 'true'

DiskEncryptionSetId DiskId   DiskType  IsOSDisk LogStorageAccountId LogStorageAccountSasSecretName  
------------------- ------   --------  -------- ------------------- ------------------------------   
                      a      Standard  true  
```

<span data-ttu-id="8b064-109">取得磁片物件以提供 New-AzMigrateServerReplication 的輸入</span><span class="sxs-lookup"><span data-stu-id="8b064-109">Get disks object to provide input for New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="8b064-110">參數</span><span class="sxs-lookup"><span data-stu-id="8b064-110">PARAMETERS</span></span>

### <span data-ttu-id="8b064-111">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="8b064-111">-DiskEncryptionSetID</span></span>
<span data-ttu-id="8b064-112">指定要使用的磁片 encyption 集。</span><span class="sxs-lookup"><span data-stu-id="8b064-112">Specifies the disk encyption set to be used.</span></span>

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

### <span data-ttu-id="8b064-113">-DiskID</span><span class="sxs-lookup"><span data-stu-id="8b064-113">-DiskID</span></span>
<span data-ttu-id="8b064-114">指定附加到已探索伺服器的磁片識別碼，以進行遷移。</span><span class="sxs-lookup"><span data-stu-id="8b064-114">Specifies the disk ID of the disk attached to the discovered server to be migrated.</span></span>

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

### <span data-ttu-id="8b064-115">-DiskType</span><span class="sxs-lookup"><span data-stu-id="8b064-115">-DiskType</span></span>
<span data-ttu-id="8b064-116">指定要用於 Azure VM 的磁片類型。</span><span class="sxs-lookup"><span data-stu-id="8b064-116">Specifies the type of disks to be used for the Azure VM.</span></span>

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

### <span data-ttu-id="8b064-117">-IsOSDisk</span><span class="sxs-lookup"><span data-stu-id="8b064-117">-IsOSDisk</span></span>
<span data-ttu-id="8b064-118">指定磁片是否包含要遷移之來源伺服器的作業系統。</span><span class="sxs-lookup"><span data-stu-id="8b064-118">Specifies whether the disk contains the Operating System for the source server to be migrated.</span></span>

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

### <span data-ttu-id="8b064-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b064-119">CommonParameters</span></span>
<span data-ttu-id="8b064-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8b064-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b064-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8b064-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b064-122">輸入</span><span class="sxs-lookup"><span data-stu-id="8b064-122">INPUTS</span></span>

## <span data-ttu-id="8b064-123">輸出</span><span class="sxs-lookup"><span data-stu-id="8b064-123">OUTPUTS</span></span>

### <span data-ttu-id="8b064-124">IVMwareCbtDiskInput 中的 Api20180110 （）。</span><span class="sxs-lookup"><span data-stu-id="8b064-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span></span>

## <span data-ttu-id="8b064-125">筆記</span><span class="sxs-lookup"><span data-stu-id="8b064-125">NOTES</span></span>

<span data-ttu-id="8b064-126">別名</span><span class="sxs-lookup"><span data-stu-id="8b064-126">ALIASES</span></span>

## <span data-ttu-id="8b064-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="8b064-127">RELATED LINKS</span></span>

