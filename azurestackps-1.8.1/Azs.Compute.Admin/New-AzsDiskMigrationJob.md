---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: db6eff0b0b0e0698c42dd7905cd3e5f7879345e1
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93793883"
---
# <span data-ttu-id="aac25-101">New-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="aac25-101">New-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="aac25-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aac25-102">SYNOPSIS</span></span>
<span data-ttu-id="aac25-103">啟動受管理的磁片遷移作業，以將受管理的磁片遷移至指定的目的地共用。</span><span class="sxs-lookup"><span data-stu-id="aac25-103">Starts a managed disk migration job to migrate managed disks to the specified destination share.</span></span>

## <span data-ttu-id="aac25-104">句法</span><span class="sxs-lookup"><span data-stu-id="aac25-104">SYNTAX</span></span>

```
New-AzsDiskMigrationJob [-Disks] <Disk[]> [-TargetShare] <String> [[-Location] <String>] [-Name] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="aac25-105">說明</span><span class="sxs-lookup"><span data-stu-id="aac25-105">DESCRIPTION</span></span>
<span data-ttu-id="aac25-106">建立磁片遷移作業。</span><span class="sxs-lookup"><span data-stu-id="aac25-106">Create a disk migration job.</span></span>

## <span data-ttu-id="aac25-107">示例</span><span class="sxs-lookup"><span data-stu-id="aac25-107">EXAMPLES</span></span>

### <span data-ttu-id="aac25-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="aac25-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsDiskMigrationJob -Name "MyMigrationJob" -Disks $disks -location local -TargetShare "\\SU1FileServer.azurestack.local\SU1_ObjStore"
```

<span data-ttu-id="aac25-109">啟動前20個磁片的受管理磁片遷移作業</span><span class="sxs-lookup"><span data-stu-id="aac25-109">Start a managed disk migration job for the first 20 disks</span></span>

## <span data-ttu-id="aac25-110">參數</span><span class="sxs-lookup"><span data-stu-id="aac25-110">PARAMETERS</span></span>

### <span data-ttu-id="aac25-111">-磁片</span><span class="sxs-lookup"><span data-stu-id="aac25-111">-Disks</span></span>
<span data-ttu-id="aac25-112">磁片清單的參數。</span><span class="sxs-lookup"><span data-stu-id="aac25-112">The parameters of disk list.</span></span>

```yaml
Type: Disk[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aac25-113">-位置</span><span class="sxs-lookup"><span data-stu-id="aac25-113">-Location</span></span>
<span data-ttu-id="aac25-114">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="aac25-114">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aac25-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="aac25-115">-Name</span></span>
<span data-ttu-id="aac25-116">[遷移作業 guid] 名稱。</span><span class="sxs-lookup"><span data-stu-id="aac25-116">The migration job guid name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: MigrationId

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aac25-117">-TargetShare</span><span class="sxs-lookup"><span data-stu-id="aac25-117">-TargetShare</span></span>
<span data-ttu-id="aac25-118">目標共用名稱稱。</span><span class="sxs-lookup"><span data-stu-id="aac25-118">The target share name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aac25-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aac25-119">CommonParameters</span></span>
<span data-ttu-id="aac25-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aac25-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aac25-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="aac25-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aac25-122">輸入</span><span class="sxs-lookup"><span data-stu-id="aac25-122">INPUTS</span></span>

## <span data-ttu-id="aac25-123">輸出</span><span class="sxs-lookup"><span data-stu-id="aac25-123">OUTPUTS</span></span>

### <span data-ttu-id="aac25-124">AzureStack （DiskMigrationJob）的計算。</span><span class="sxs-lookup"><span data-stu-id="aac25-124">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="aac25-125">筆記</span><span class="sxs-lookup"><span data-stu-id="aac25-125">NOTES</span></span>

## <span data-ttu-id="aac25-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="aac25-126">RELATED LINKS</span></span>
