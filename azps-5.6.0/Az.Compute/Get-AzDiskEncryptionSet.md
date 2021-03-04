---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
ms.openlocfilehash: 344bba00d610b5e23b2af5bce8476185e8bee377
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906250"
---
# <span data-ttu-id="c8e26-101">Get-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="c8e26-101">Get-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="c8e26-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c8e26-102">SYNOPSIS</span></span>
<span data-ttu-id="c8e26-103">取得或列出磁片加密集。</span><span class="sxs-lookup"><span data-stu-id="c8e26-103">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="c8e26-104">語法</span><span class="sxs-lookup"><span data-stu-id="c8e26-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8e26-105">描述</span><span class="sxs-lookup"><span data-stu-id="c8e26-105">DESCRIPTION</span></span>
<span data-ttu-id="c8e26-106">取得或列出磁片加密集。</span><span class="sxs-lookup"><span data-stu-id="c8e26-106">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="c8e26-107">例子</span><span class="sxs-lookup"><span data-stu-id="c8e26-107">EXAMPLES</span></span>

### <span data-ttu-id="c8e26-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="c8e26-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSet -ResourceGroupName rg1 -Name enc1;

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc1
Name              : enc1
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}
```

<span data-ttu-id="c8e26-109">取得磁片加密集 'enc1'</span><span class="sxs-lookup"><span data-stu-id="c8e26-109">Get disk encryption set 'enc1'</span></span>

### <span data-ttu-id="c8e26-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="c8e26-110">Example 2</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSet

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc1
Name              : enc1
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc2
Name              : enc2
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}
```

<span data-ttu-id="c8e26-111">取得資源群組 'rg1' 中所有的磁片加密集。</span><span class="sxs-lookup"><span data-stu-id="c8e26-111">Get all disk encryption sets in resource group 'rg1'.</span></span>

### <span data-ttu-id="c8e26-112">範例 3</span><span class="sxs-lookup"><span data-stu-id="c8e26-112">Example 3</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSet -ResourceGroupName rg1

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc1
Name              : enc1
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc2
Name              : enc2
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}

ResourceGroupName : rg2
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc3
Name              : enc3
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}
```

<span data-ttu-id="c8e26-113">取得訂閱中所有的磁片加密集。</span><span class="sxs-lookup"><span data-stu-id="c8e26-113">Get all disk encryption sets in subscription.</span></span>

## <span data-ttu-id="c8e26-114">參數</span><span class="sxs-lookup"><span data-stu-id="c8e26-114">PARAMETERS</span></span>

### <span data-ttu-id="c8e26-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8e26-115">-DefaultProfile</span></span>
<span data-ttu-id="c8e26-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c8e26-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8e26-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="c8e26-117">-Name</span></span>
<span data-ttu-id="c8e26-118">磁片加密集的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8e26-118">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskEncryptionSetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8e26-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8e26-119">-ResourceGroupName</span></span>
<span data-ttu-id="c8e26-120">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8e26-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8e26-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8e26-121">CommonParameters</span></span>
<span data-ttu-id="c8e26-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c8e26-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8e26-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8e26-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8e26-124">輸入</span><span class="sxs-lookup"><span data-stu-id="c8e26-124">INPUTS</span></span>

### <span data-ttu-id="c8e26-125">System.String</span><span class="sxs-lookup"><span data-stu-id="c8e26-125">System.String</span></span>

## <span data-ttu-id="c8e26-126">輸出</span><span class="sxs-lookup"><span data-stu-id="c8e26-126">OUTPUTS</span></span>

### <span data-ttu-id="c8e26-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="c8e26-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="c8e26-128">筆記</span><span class="sxs-lookup"><span data-stu-id="c8e26-128">NOTES</span></span>

## <span data-ttu-id="c8e26-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8e26-129">RELATED LINKS</span></span>
