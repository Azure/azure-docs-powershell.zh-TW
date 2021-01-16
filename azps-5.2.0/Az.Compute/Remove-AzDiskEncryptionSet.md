---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
ms.openlocfilehash: a15dd51bad097aafcc517fbef67f89d65b076380
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283443"
---
# <span data-ttu-id="ec754-101">Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="ec754-101">Remove-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="ec754-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ec754-102">SYNOPSIS</span></span>
<span data-ttu-id="ec754-103">移除磁片加密集。</span><span class="sxs-lookup"><span data-stu-id="ec754-103">Removes a disk encryption set.</span></span>

## <span data-ttu-id="ec754-104">句法</span><span class="sxs-lookup"><span data-stu-id="ec754-104">SYNTAX</span></span>

### <span data-ttu-id="ec754-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="ec754-105">DefaultParameter (Default)</span></span>
```
Remove-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec754-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="ec754-106">ResourceIdParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec754-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="ec754-107">ObjectParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-InputObject] <PSDiskEncryptionSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec754-108">說明</span><span class="sxs-lookup"><span data-stu-id="ec754-108">DESCRIPTION</span></span>
<span data-ttu-id="ec754-109">移除磁片加密集。</span><span class="sxs-lookup"><span data-stu-id="ec754-109">Removes a disk encryption set.</span></span>

## <span data-ttu-id="ec754-110">示例</span><span class="sxs-lookup"><span data-stu-id="ec754-110">EXAMPLES</span></span>

### <span data-ttu-id="ec754-111">範例1</span><span class="sxs-lookup"><span data-stu-id="ec754-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -Force;
```

<span data-ttu-id="ec754-112">刪除 "rg1" 中的磁片加密集 "enc1"</span><span class="sxs-lookup"><span data-stu-id="ec754-112">Delete disk encryption set 'enc1' in 'rg1'</span></span>

## <span data-ttu-id="ec754-113">參數</span><span class="sxs-lookup"><span data-stu-id="ec754-113">PARAMETERS</span></span>

### <span data-ttu-id="ec754-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec754-114">-AsJob</span></span>
<span data-ttu-id="ec754-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ec754-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ec754-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec754-116">-DefaultProfile</span></span>
<span data-ttu-id="ec754-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ec754-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec754-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ec754-118">-Force</span></span>
<span data-ttu-id="ec754-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="ec754-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ec754-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec754-120">-InputObject</span></span>
<span data-ttu-id="ec754-121">磁片加密集的本機物件。</span><span class="sxs-lookup"><span data-stu-id="ec754-121">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: ObjectParameter
Aliases: DiskEncryptionSet

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec754-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="ec754-122">-Name</span></span>
<span data-ttu-id="ec754-123">磁片加密集的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec754-123">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec754-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec754-124">-ResourceGroupName</span></span>
<span data-ttu-id="ec754-125">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec754-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec754-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec754-126">-ResourceId</span></span>
<span data-ttu-id="ec754-127">資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ec754-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec754-128">-確認</span><span class="sxs-lookup"><span data-stu-id="ec754-128">-Confirm</span></span>
<span data-ttu-id="ec754-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ec754-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec754-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec754-130">-WhatIf</span></span>
<span data-ttu-id="ec754-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ec754-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec754-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ec754-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec754-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec754-133">CommonParameters</span></span>
<span data-ttu-id="ec754-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ec754-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec754-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ec754-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec754-136">輸入</span><span class="sxs-lookup"><span data-stu-id="ec754-136">INPUTS</span></span>

### <span data-ttu-id="ec754-137">System.object</span><span class="sxs-lookup"><span data-stu-id="ec754-137">System.String</span></span>

### <span data-ttu-id="ec754-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="ec754-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="ec754-139">輸出</span><span class="sxs-lookup"><span data-stu-id="ec754-139">OUTPUTS</span></span>

### <span data-ttu-id="ec754-140">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="ec754-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="ec754-141">筆記</span><span class="sxs-lookup"><span data-stu-id="ec754-141">NOTES</span></span>

## <span data-ttu-id="ec754-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec754-142">RELATED LINKS</span></span>
