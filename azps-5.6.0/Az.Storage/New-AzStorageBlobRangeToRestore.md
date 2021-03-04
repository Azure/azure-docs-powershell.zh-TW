---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: 0f74ad9b146a0c5d2f2c65b7109fb57f56902834
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915102"
---
# <span data-ttu-id="2c67e-101">New-AzStorageBlobRangeToRestore</span><span class="sxs-lookup"><span data-stu-id="2c67e-101">New-AzStorageBlobRangeToRestore</span></span>

## <span data-ttu-id="2c67e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2c67e-102">SYNOPSIS</span></span>
<span data-ttu-id="2c67e-103">建立 Blob 範圍物件以還原儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="2c67e-103">Creates a Blob Range object to restores a Storage account.</span></span>

## <span data-ttu-id="2c67e-104">語法</span><span class="sxs-lookup"><span data-stu-id="2c67e-104">SYNTAX</span></span>

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c67e-105">描述</span><span class="sxs-lookup"><span data-stu-id="2c67e-105">DESCRIPTION</span></span>
<span data-ttu-id="2c67e-106">**New-AzStorageBlobRangeToRestore** Cmdlet 會建立 Blob 範圍物件，可用於 Restore-AzStorageBlobRange。</span><span class="sxs-lookup"><span data-stu-id="2c67e-106">The **New-AzStorageBlobRangeToRestore** cmdlet creates a Blob range object, which can be used in Restore-AzStorageBlobRange.</span></span>

## <span data-ttu-id="2c67e-107">例子</span><span class="sxs-lookup"><span data-stu-id="2c67e-107">EXAMPLES</span></span>

### <span data-ttu-id="2c67e-108">範例 1：建立 Blob 範圍以還原</span><span class="sxs-lookup"><span data-stu-id="2c67e-108">Example 1: Creates a blob range to restore</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

<span data-ttu-id="2c67e-109">此命令會建立要還原的 blob 範圍，從 container1/blob1 開始， (包含) ，結尾是 container2/blob2 (排除) 。</span><span class="sxs-lookup"><span data-stu-id="2c67e-109">This command creates a blob range to restore, which starts at container1/blob1 (include), and ends at container2/blob2 (exclude).</span></span>

### <span data-ttu-id="2c67e-110">範例 2：建立 Blob 範圍，以字母順序從第一個 Blob 還原到特定的 blob， (排除) </span><span class="sxs-lookup"><span data-stu-id="2c67e-110">Example 2: Creates a blob range which will restore from first blob in alphabetical order, to a specific blob (exclude)</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

<span data-ttu-id="2c67e-111">此命令會建立 Blob 範圍，從第一個按字母順序的 Blob 還原到特定的 Blob 容器2/blob2， (排除) </span><span class="sxs-lookup"><span data-stu-id="2c67e-111">This command creates a blob range which will restore from first blob of alphabetical order, to a specific blob container2/blob2 (exclude)</span></span>

### <span data-ttu-id="2c67e-112">範例 3：建立 Blob 範圍，該範圍會從特定的 blob (包含) ，還原到最後一個 blob，並按字母順序</span><span class="sxs-lookup"><span data-stu-id="2c67e-112">Example 3: Creates a blob range which will restore from a specific blob (include), to the last blob in alphabetical order</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

<span data-ttu-id="2c67e-113">此命令會建立 Blob 範圍，從特定的 Blob 容器1/blob1 (包含) ，以字母順序還原到最後一個 Blob。</span><span class="sxs-lookup"><span data-stu-id="2c67e-113">This command creates a blob range which will restore from a specific blob container1/blob1 (include), to the last blob in alphabetical order.</span></span>

### <span data-ttu-id="2c67e-114">範例 4：建立 Blob 範圍以還原所有 Blob</span><span class="sxs-lookup"><span data-stu-id="2c67e-114">Example 4: Creates a blob range which will restore all blobs</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

<span data-ttu-id="2c67e-115">此命令會建立一個 Blob 範圍，可還原所有 Blob。</span><span class="sxs-lookup"><span data-stu-id="2c67e-115">This command creates a blob range which will restore all blobs.</span></span>

## <span data-ttu-id="2c67e-116">參數</span><span class="sxs-lookup"><span data-stu-id="2c67e-116">PARAMETERS</span></span>

### <span data-ttu-id="2c67e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c67e-117">-DefaultProfile</span></span>
<span data-ttu-id="2c67e-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2c67e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c67e-119">-EndRange</span><span class="sxs-lookup"><span data-stu-id="2c67e-119">-EndRange</span></span>
<span data-ttu-id="2c67e-120">指定 Blob 還原結束範圍。</span><span class="sxs-lookup"><span data-stu-id="2c67e-120">Specify the blob restore End range.</span></span>
<span data-ttu-id="2c67e-121">還原 Blob 中會排除結束範圍。</span><span class="sxs-lookup"><span data-stu-id="2c67e-121">End range will be excluded in restore blobs.</span></span>
<span data-ttu-id="2c67e-122">將其設定為空白字串以還原到結尾。</span><span class="sxs-lookup"><span data-stu-id="2c67e-122">Set it as empty strng to restore to the end.</span></span>

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

### <span data-ttu-id="2c67e-123">-StartRange</span><span class="sxs-lookup"><span data-stu-id="2c67e-123">-StartRange</span></span>
<span data-ttu-id="2c67e-124">指定 Blob 還原開始範圍。</span><span class="sxs-lookup"><span data-stu-id="2c67e-124">Specify the blob restore start range.</span></span>
<span data-ttu-id="2c67e-125">還原 Blob 中會包含開始範圍。</span><span class="sxs-lookup"><span data-stu-id="2c67e-125">Start range will be included in restore blobs.</span></span>
<span data-ttu-id="2c67e-126">將其設定為空白字串，以從頭開始還原。</span><span class="sxs-lookup"><span data-stu-id="2c67e-126">Set it as empty string to restore from begining.</span></span>

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

### <span data-ttu-id="2c67e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c67e-127">CommonParameters</span></span>
<span data-ttu-id="2c67e-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2c67e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c67e-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="2c67e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c67e-130">輸入</span><span class="sxs-lookup"><span data-stu-id="2c67e-130">INPUTS</span></span>

### <span data-ttu-id="2c67e-131">沒有</span><span class="sxs-lookup"><span data-stu-id="2c67e-131">None</span></span>

## <span data-ttu-id="2c67e-132">輸出</span><span class="sxs-lookup"><span data-stu-id="2c67e-132">OUTPUTS</span></span>

### <span data-ttu-id="2c67e-133">Microsoft.Azure.Commands.management.storage.models.PSBlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="2c67e-133">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange</span></span>

## <span data-ttu-id="2c67e-134">筆記</span><span class="sxs-lookup"><span data-stu-id="2c67e-134">NOTES</span></span>

## <span data-ttu-id="2c67e-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c67e-135">RELATED LINKS</span></span>
