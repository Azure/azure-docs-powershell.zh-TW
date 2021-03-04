---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSetAssociatedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSetAssociatedResource.md
ms.openlocfilehash: f85b1ffb181a277e750d6f6f4a67ef55ad2a75bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906246"
---
# <span data-ttu-id="836f7-101">Get-AzDiskEncryptionSetAssociatedResource</span><span class="sxs-lookup"><span data-stu-id="836f7-101">Get-AzDiskEncryptionSetAssociatedResource</span></span>

## <span data-ttu-id="836f7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="836f7-102">SYNOPSIS</span></span>
<span data-ttu-id="836f7-103">獲得與指定的磁片加密集相關聯的資源清單。</span><span class="sxs-lookup"><span data-stu-id="836f7-103">Gets the list of resources associated with the specified disk encryption set.</span></span>

## <span data-ttu-id="836f7-104">語法</span><span class="sxs-lookup"><span data-stu-id="836f7-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSetAssociatedResource [-ResourceGroupName] <String> [-DiskEncryptionSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="836f7-105">描述</span><span class="sxs-lookup"><span data-stu-id="836f7-105">DESCRIPTION</span></span>
<span data-ttu-id="836f7-106">**Get-AzCryptEncryptionSetAssociatedResource** Cmdlet 會取得與指定的磁片加密集相關聯的資源清單。</span><span class="sxs-lookup"><span data-stu-id="836f7-106">The **Get-AzDiskEncryptionSetAssociatedResource** cmdlet gets the list of resources associated with the specified disk encryption set.</span></span>

## <span data-ttu-id="836f7-107">例子</span><span class="sxs-lookup"><span data-stu-id="836f7-107">EXAMPLES</span></span>

### <span data-ttu-id="836f7-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="836f7-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSetAssociatedResource -ResourceGroupName $RGname -DiskEncryptionSetName $diskEncryptionSetName

/subscriptions/xxxxx-xxx-xx/resourceGroups/exampleResourceGroup/providers/Microsoft.Compute/disks/exampleDisk01
/subscriptions/xxxxx-xxx-xx/resourceGroups/exampleResourceGroup/providers/Microsoft.Compute/disks/exmapleDisk02
```

<span data-ttu-id="836f7-109">Cmdlet 會取回與所提供的磁片加密集相關聯的兩個資源，"example Disk01" 和 "example Disk02"。</span><span class="sxs-lookup"><span data-stu-id="836f7-109">The cmdlet retrieves the two resources, 'exampleDisk01' and 'exampleDisk02', associated with the provided Disk Encryption Set</span></span>

## <span data-ttu-id="836f7-110">參數</span><span class="sxs-lookup"><span data-stu-id="836f7-110">PARAMETERS</span></span>

### <span data-ttu-id="836f7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="836f7-111">-DefaultProfile</span></span>
<span data-ttu-id="836f7-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="836f7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="836f7-113">-DiskEncryptionSetName</span><span class="sxs-lookup"><span data-stu-id="836f7-113">-DiskEncryptionSetName</span></span>
<span data-ttu-id="836f7-114">磁片加密集的名稱。</span><span class="sxs-lookup"><span data-stu-id="836f7-114">Name of disk encryption set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="836f7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="836f7-115">-ResourceGroupName</span></span>
<span data-ttu-id="836f7-116">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="836f7-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="836f7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="836f7-117">CommonParameters</span></span>
<span data-ttu-id="836f7-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="836f7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="836f7-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="836f7-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="836f7-120">輸入</span><span class="sxs-lookup"><span data-stu-id="836f7-120">INPUTS</span></span>

### <span data-ttu-id="836f7-121">System.String</span><span class="sxs-lookup"><span data-stu-id="836f7-121">System.String</span></span>

## <span data-ttu-id="836f7-122">輸出</span><span class="sxs-lookup"><span data-stu-id="836f7-122">OUTPUTS</span></span>

### <span data-ttu-id="836f7-123">System.Uri[]</span><span class="sxs-lookup"><span data-stu-id="836f7-123">System.Uri[]</span></span>

## <span data-ttu-id="836f7-124">筆記</span><span class="sxs-lookup"><span data-stu-id="836f7-124">NOTES</span></span>

## <span data-ttu-id="836f7-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="836f7-125">RELATED LINKS</span></span>
