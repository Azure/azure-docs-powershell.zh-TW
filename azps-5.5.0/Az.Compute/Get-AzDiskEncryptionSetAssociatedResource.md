---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSetAssociatedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSetAssociatedResource.md
ms.openlocfilehash: f85b1ffb181a277e750d6f6f4a67ef55ad2a75bc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129875"
---
# <span data-ttu-id="adffe-101">Get-AzDiskEncryptionSetAssociatedResource</span><span class="sxs-lookup"><span data-stu-id="adffe-101">Get-AzDiskEncryptionSetAssociatedResource</span></span>

## <span data-ttu-id="adffe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="adffe-102">SYNOPSIS</span></span>
<span data-ttu-id="adffe-103">取得與指定磁片加密集相關聯的資源清單。</span><span class="sxs-lookup"><span data-stu-id="adffe-103">Gets the list of resources associated with the specified disk encryption set.</span></span>

## <span data-ttu-id="adffe-104">句法</span><span class="sxs-lookup"><span data-stu-id="adffe-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSetAssociatedResource [-ResourceGroupName] <String> [-DiskEncryptionSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adffe-105">說明</span><span class="sxs-lookup"><span data-stu-id="adffe-105">DESCRIPTION</span></span>
<span data-ttu-id="adffe-106">**AzDiskEncryptionSetAssociatedResource** Cmdlet 會取得與指定磁片加密集相關聯的資源清單。</span><span class="sxs-lookup"><span data-stu-id="adffe-106">The **Get-AzDiskEncryptionSetAssociatedResource** cmdlet gets the list of resources associated with the specified disk encryption set.</span></span>

## <span data-ttu-id="adffe-107">示例</span><span class="sxs-lookup"><span data-stu-id="adffe-107">EXAMPLES</span></span>

### <span data-ttu-id="adffe-108">範例1</span><span class="sxs-lookup"><span data-stu-id="adffe-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSetAssociatedResource -ResourceGroupName $RGname -DiskEncryptionSetName $diskEncryptionSetName

/subscriptions/xxxxx-xxx-xx/resourceGroups/exampleResourceGroup/providers/Microsoft.Compute/disks/exampleDisk01
/subscriptions/xxxxx-xxx-xx/resourceGroups/exampleResourceGroup/providers/Microsoft.Compute/disks/exmapleDisk02
```

<span data-ttu-id="adffe-109">Cmdlet 會檢索與所提供磁片加密集相關聯的兩個資源（"exampleDisk01" 和 "exampleDisk02"）</span><span class="sxs-lookup"><span data-stu-id="adffe-109">The cmdlet retrieves the two resources, 'exampleDisk01' and 'exampleDisk02', associated with the provided Disk Encryption Set</span></span>

## <span data-ttu-id="adffe-110">參數</span><span class="sxs-lookup"><span data-stu-id="adffe-110">PARAMETERS</span></span>

### <span data-ttu-id="adffe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adffe-111">-DefaultProfile</span></span>
<span data-ttu-id="adffe-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="adffe-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adffe-113">-DiskEncryptionSetName</span><span class="sxs-lookup"><span data-stu-id="adffe-113">-DiskEncryptionSetName</span></span>
<span data-ttu-id="adffe-114">磁片加密集的名稱。</span><span class="sxs-lookup"><span data-stu-id="adffe-114">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="adffe-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adffe-115">-ResourceGroupName</span></span>
<span data-ttu-id="adffe-116">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="adffe-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="adffe-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adffe-117">CommonParameters</span></span>
<span data-ttu-id="adffe-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="adffe-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adffe-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="adffe-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adffe-120">輸入</span><span class="sxs-lookup"><span data-stu-id="adffe-120">INPUTS</span></span>

### <span data-ttu-id="adffe-121">System.object</span><span class="sxs-lookup"><span data-stu-id="adffe-121">System.String</span></span>

## <span data-ttu-id="adffe-122">輸出</span><span class="sxs-lookup"><span data-stu-id="adffe-122">OUTPUTS</span></span>

### <span data-ttu-id="adffe-123">System.object []</span><span class="sxs-lookup"><span data-stu-id="adffe-123">System.Uri[]</span></span>

## <span data-ttu-id="adffe-124">筆記</span><span class="sxs-lookup"><span data-stu-id="adffe-124">NOTES</span></span>

## <span data-ttu-id="adffe-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="adffe-125">RELATED LINKS</span></span>
