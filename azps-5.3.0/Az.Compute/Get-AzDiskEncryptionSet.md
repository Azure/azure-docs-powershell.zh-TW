---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
ms.openlocfilehash: 7d2b23c08f7ce910daf87f7cebbea844d5bda6f0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98446471"
---
# <span data-ttu-id="65965-101">Get-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="65965-101">Get-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="65965-102">摘要</span><span class="sxs-lookup"><span data-stu-id="65965-102">SYNOPSIS</span></span>
<span data-ttu-id="65965-103">取得或列出磁片加密集。</span><span class="sxs-lookup"><span data-stu-id="65965-103">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="65965-104">句法</span><span class="sxs-lookup"><span data-stu-id="65965-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65965-105">說明</span><span class="sxs-lookup"><span data-stu-id="65965-105">DESCRIPTION</span></span>
<span data-ttu-id="65965-106">取得或列出磁片加密集。</span><span class="sxs-lookup"><span data-stu-id="65965-106">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="65965-107">示例</span><span class="sxs-lookup"><span data-stu-id="65965-107">EXAMPLES</span></span>

### <span data-ttu-id="65965-108">範例1</span><span class="sxs-lookup"><span data-stu-id="65965-108">Example 1</span></span>
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

<span data-ttu-id="65965-109">取得磁片加密設定 ' enc1」</span><span class="sxs-lookup"><span data-stu-id="65965-109">Get disk encryption set 'enc1'</span></span>

### <span data-ttu-id="65965-110">範例2</span><span class="sxs-lookup"><span data-stu-id="65965-110">Example 2</span></span>
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

<span data-ttu-id="65965-111">取得資源群組 ' rg1」中的所有磁片加密集。</span><span class="sxs-lookup"><span data-stu-id="65965-111">Get all disk encryption sets in resource group 'rg1'.</span></span>

### <span data-ttu-id="65965-112">範例3</span><span class="sxs-lookup"><span data-stu-id="65965-112">Example 3</span></span>
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

<span data-ttu-id="65965-113">取得訂閱中的所有磁片加密集。</span><span class="sxs-lookup"><span data-stu-id="65965-113">Get all disk encryption sets in subscription.</span></span>

## <span data-ttu-id="65965-114">參數</span><span class="sxs-lookup"><span data-stu-id="65965-114">PARAMETERS</span></span>

### <span data-ttu-id="65965-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65965-115">-DefaultProfile</span></span>
<span data-ttu-id="65965-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="65965-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65965-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="65965-117">-Name</span></span>
<span data-ttu-id="65965-118">磁片加密集的名稱。</span><span class="sxs-lookup"><span data-stu-id="65965-118">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="65965-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65965-119">-ResourceGroupName</span></span>
<span data-ttu-id="65965-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="65965-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="65965-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65965-121">CommonParameters</span></span>
<span data-ttu-id="65965-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="65965-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65965-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="65965-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65965-124">輸入</span><span class="sxs-lookup"><span data-stu-id="65965-124">INPUTS</span></span>

### <span data-ttu-id="65965-125">System.object</span><span class="sxs-lookup"><span data-stu-id="65965-125">System.String</span></span>

## <span data-ttu-id="65965-126">輸出</span><span class="sxs-lookup"><span data-stu-id="65965-126">OUTPUTS</span></span>

### <span data-ttu-id="65965-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="65965-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="65965-128">筆記</span><span class="sxs-lookup"><span data-stu-id="65965-128">NOTES</span></span>

## <span data-ttu-id="65965-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="65965-129">RELATED LINKS</span></span>
