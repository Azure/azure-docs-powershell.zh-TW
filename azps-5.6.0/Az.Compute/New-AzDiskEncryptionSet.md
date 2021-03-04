---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
ms.openlocfilehash: 3e2e04e2e489b9c9322c62d1c7006490d7bf9bd2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903325"
---
# <span data-ttu-id="df1da-101">New-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="df1da-101">New-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="df1da-102">簡介</span><span class="sxs-lookup"><span data-stu-id="df1da-102">SYNOPSIS</span></span>
<span data-ttu-id="df1da-103">建立磁片加密集。</span><span class="sxs-lookup"><span data-stu-id="df1da-103">Creates a disk encryption set.</span></span>

## <span data-ttu-id="df1da-104">語法</span><span class="sxs-lookup"><span data-stu-id="df1da-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-InputObject] <PSDiskEncryptionSet>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df1da-105">描述</span><span class="sxs-lookup"><span data-stu-id="df1da-105">DESCRIPTION</span></span>
<span data-ttu-id="df1da-106">建立磁片加密集。</span><span class="sxs-lookup"><span data-stu-id="df1da-106">Creates a disk encryption set.</span></span>

## <span data-ttu-id="df1da-107">例子</span><span class="sxs-lookup"><span data-stu-id="df1da-107">EXAMPLES</span></span>

### <span data-ttu-id="df1da-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="df1da-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="df1da-109">使用金鑰庫中的已使用金鑰建立磁片加密集。</span><span class="sxs-lookup"><span data-stu-id="df1da-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="df1da-110">參數</span><span class="sxs-lookup"><span data-stu-id="df1da-110">PARAMETERS</span></span>

### <span data-ttu-id="df1da-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df1da-111">-AsJob</span></span>
<span data-ttu-id="df1da-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="df1da-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df1da-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df1da-113">-DefaultProfile</span></span>
<span data-ttu-id="df1da-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="df1da-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df1da-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df1da-115">-InputObject</span></span>
<span data-ttu-id="df1da-116">磁片加密集的本機物件。</span><span class="sxs-lookup"><span data-stu-id="df1da-116">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: (All)
Aliases: DiskEncryptionSet

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df1da-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="df1da-117">-Name</span></span>
<span data-ttu-id="df1da-118">磁片加密集的名稱。</span><span class="sxs-lookup"><span data-stu-id="df1da-118">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df1da-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df1da-119">-ResourceGroupName</span></span>
<span data-ttu-id="df1da-120">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="df1da-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df1da-121">-確認</span><span class="sxs-lookup"><span data-stu-id="df1da-121">-Confirm</span></span>
<span data-ttu-id="df1da-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="df1da-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df1da-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df1da-123">-WhatIf</span></span>
<span data-ttu-id="df1da-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="df1da-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df1da-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="df1da-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df1da-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df1da-126">CommonParameters</span></span>
<span data-ttu-id="df1da-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="df1da-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df1da-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df1da-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df1da-129">輸入</span><span class="sxs-lookup"><span data-stu-id="df1da-129">INPUTS</span></span>

### <span data-ttu-id="df1da-130">System.String</span><span class="sxs-lookup"><span data-stu-id="df1da-130">System.String</span></span>

### <span data-ttu-id="df1da-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="df1da-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="df1da-132">輸出</span><span class="sxs-lookup"><span data-stu-id="df1da-132">OUTPUTS</span></span>

### <span data-ttu-id="df1da-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="df1da-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="df1da-134">筆記</span><span class="sxs-lookup"><span data-stu-id="df1da-134">NOTES</span></span>

## <span data-ttu-id="df1da-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="df1da-135">RELATED LINKS</span></span>
