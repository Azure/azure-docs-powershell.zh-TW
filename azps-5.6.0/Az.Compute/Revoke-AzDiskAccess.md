---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/revoke-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
ms.openlocfilehash: 767104edb73265f472e155e8d003b0b5e96906e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904729"
---
# <span data-ttu-id="19799-101">Revoke-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="19799-101">Revoke-AzDiskAccess</span></span>

## <span data-ttu-id="19799-102">簡介</span><span class="sxs-lookup"><span data-stu-id="19799-102">SYNOPSIS</span></span>
<span data-ttu-id="19799-103">撤銷磁片的存取權。</span><span class="sxs-lookup"><span data-stu-id="19799-103">Revokes an access to a disk.</span></span>

## <span data-ttu-id="19799-104">語法</span><span class="sxs-lookup"><span data-stu-id="19799-104">SYNTAX</span></span>

```
Revoke-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19799-105">描述</span><span class="sxs-lookup"><span data-stu-id="19799-105">DESCRIPTION</span></span>
<span data-ttu-id="19799-106">**Revoke-Az RevokeAccess** Cmdlet 會撤銷磁片的存取權。</span><span class="sxs-lookup"><span data-stu-id="19799-106">The **Revoke-AzDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="19799-107">例子</span><span class="sxs-lookup"><span data-stu-id="19799-107">EXAMPLES</span></span>

### <span data-ttu-id="19799-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="19799-108">Example 1</span></span>
```
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="19799-109">撤銷名稱為 'ResourceGroup01' 的資源群組中名為 'Disk01' 的磁片存取權</span><span class="sxs-lookup"><span data-stu-id="19799-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="19799-110">參數</span><span class="sxs-lookup"><span data-stu-id="19799-110">PARAMETERS</span></span>

### <span data-ttu-id="19799-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19799-111">-AsJob</span></span>
<span data-ttu-id="19799-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="19799-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="19799-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19799-113">-DefaultProfile</span></span>
<span data-ttu-id="19799-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="19799-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19799-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="19799-115">-DiskName</span></span>
<span data-ttu-id="19799-116">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="19799-116">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19799-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19799-117">-ResourceGroupName</span></span>
<span data-ttu-id="19799-118">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="19799-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="19799-119">-確認</span><span class="sxs-lookup"><span data-stu-id="19799-119">-Confirm</span></span>
<span data-ttu-id="19799-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="19799-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19799-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19799-121">-WhatIf</span></span>
<span data-ttu-id="19799-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="19799-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19799-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="19799-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19799-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19799-124">CommonParameters</span></span>
<span data-ttu-id="19799-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="19799-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19799-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19799-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19799-127">輸入</span><span class="sxs-lookup"><span data-stu-id="19799-127">INPUTS</span></span>

### <span data-ttu-id="19799-128">System.String</span><span class="sxs-lookup"><span data-stu-id="19799-128">System.String</span></span>

## <span data-ttu-id="19799-129">輸出</span><span class="sxs-lookup"><span data-stu-id="19799-129">OUTPUTS</span></span>

### <span data-ttu-id="19799-130">Microsoft.Azure.Commands.Compute.Automation.models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="19799-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="19799-131">筆記</span><span class="sxs-lookup"><span data-stu-id="19799-131">NOTES</span></span>

## <span data-ttu-id="19799-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="19799-132">RELATED LINKS</span></span>
