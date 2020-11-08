---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
ms.openlocfilehash: 61d8d60925eb1d7e71ca85f92e30516d598facdf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137693"
---
# <span data-ttu-id="1543f-101">New-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="1543f-101">New-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="1543f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1543f-102">SYNOPSIS</span></span>
<span data-ttu-id="1543f-103">建立磁片加密集。</span><span class="sxs-lookup"><span data-stu-id="1543f-103">Creates a disk encryption set.</span></span>

## <span data-ttu-id="1543f-104">句法</span><span class="sxs-lookup"><span data-stu-id="1543f-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-InputObject] <PSDiskEncryptionSet>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1543f-105">說明</span><span class="sxs-lookup"><span data-stu-id="1543f-105">DESCRIPTION</span></span>
<span data-ttu-id="1543f-106">建立磁片加密集。</span><span class="sxs-lookup"><span data-stu-id="1543f-106">Creates a disk encryption set.</span></span>

## <span data-ttu-id="1543f-107">示例</span><span class="sxs-lookup"><span data-stu-id="1543f-107">EXAMPLES</span></span>

### <span data-ttu-id="1543f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="1543f-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="1543f-109">使用 [金鑰保存庫] 中指定的作用中金鑰來建立磁片加密集。</span><span class="sxs-lookup"><span data-stu-id="1543f-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="1543f-110">參數</span><span class="sxs-lookup"><span data-stu-id="1543f-110">PARAMETERS</span></span>

### <span data-ttu-id="1543f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1543f-111">-AsJob</span></span>
<span data-ttu-id="1543f-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1543f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1543f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1543f-113">-DefaultProfile</span></span>
<span data-ttu-id="1543f-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1543f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1543f-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1543f-115">-InputObject</span></span>
<span data-ttu-id="1543f-116">磁片加密集的本機物件。</span><span class="sxs-lookup"><span data-stu-id="1543f-116">The local object of the disk encryption set.</span></span>

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

### <span data-ttu-id="1543f-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="1543f-117">-Name</span></span>
<span data-ttu-id="1543f-118">磁片加密集的名稱。</span><span class="sxs-lookup"><span data-stu-id="1543f-118">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="1543f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1543f-119">-ResourceGroupName</span></span>
<span data-ttu-id="1543f-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1543f-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1543f-121">-確認</span><span class="sxs-lookup"><span data-stu-id="1543f-121">-Confirm</span></span>
<span data-ttu-id="1543f-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1543f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1543f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1543f-123">-WhatIf</span></span>
<span data-ttu-id="1543f-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1543f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1543f-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1543f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1543f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1543f-126">CommonParameters</span></span>
<span data-ttu-id="1543f-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1543f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1543f-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1543f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1543f-129">輸入</span><span class="sxs-lookup"><span data-stu-id="1543f-129">INPUTS</span></span>

### <span data-ttu-id="1543f-130">System.object</span><span class="sxs-lookup"><span data-stu-id="1543f-130">System.String</span></span>

### <span data-ttu-id="1543f-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="1543f-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="1543f-132">輸出</span><span class="sxs-lookup"><span data-stu-id="1543f-132">OUTPUTS</span></span>

### <span data-ttu-id="1543f-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="1543f-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="1543f-134">筆記</span><span class="sxs-lookup"><span data-stu-id="1543f-134">NOTES</span></span>

## <span data-ttu-id="1543f-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="1543f-135">RELATED LINKS</span></span>