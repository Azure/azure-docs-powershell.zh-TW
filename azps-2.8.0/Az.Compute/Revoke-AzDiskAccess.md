---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
ms.openlocfilehash: 13ae9cc51b5a1f29b995e9dd5c98ee1243339585
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613206"
---
# <span data-ttu-id="fa2df-101">Revoke-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="fa2df-101">Revoke-AzDiskAccess</span></span>

## <span data-ttu-id="fa2df-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fa2df-102">SYNOPSIS</span></span>
<span data-ttu-id="fa2df-103">吊銷磁片存取權。</span><span class="sxs-lookup"><span data-stu-id="fa2df-103">Revokes an access to a disk.</span></span>

## <span data-ttu-id="fa2df-104">句法</span><span class="sxs-lookup"><span data-stu-id="fa2df-104">SYNTAX</span></span>

```
Revoke-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa2df-105">說明</span><span class="sxs-lookup"><span data-stu-id="fa2df-105">DESCRIPTION</span></span>
<span data-ttu-id="fa2df-106">**Revoke AzDiskAccess** Cmdlet 會吊銷磁片存取權。</span><span class="sxs-lookup"><span data-stu-id="fa2df-106">The **Revoke-AzDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="fa2df-107">示例</span><span class="sxs-lookup"><span data-stu-id="fa2df-107">EXAMPLES</span></span>

### <span data-ttu-id="fa2df-108">範例1</span><span class="sxs-lookup"><span data-stu-id="fa2df-108">Example 1</span></span>
```
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="fa2df-109">在名為 "ResourceGroup01" 的資源群組中，廢除名為「Disk01」的磁片存取權</span><span class="sxs-lookup"><span data-stu-id="fa2df-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="fa2df-110">參數</span><span class="sxs-lookup"><span data-stu-id="fa2df-110">PARAMETERS</span></span>

### <span data-ttu-id="fa2df-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa2df-111">-AsJob</span></span>
<span data-ttu-id="fa2df-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fa2df-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa2df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa2df-113">-DefaultProfile</span></span>
<span data-ttu-id="fa2df-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fa2df-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa2df-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="fa2df-115">-DiskName</span></span>
<span data-ttu-id="fa2df-116">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa2df-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="fa2df-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa2df-117">-ResourceGroupName</span></span>
<span data-ttu-id="fa2df-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa2df-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="fa2df-119">-確認</span><span class="sxs-lookup"><span data-stu-id="fa2df-119">-Confirm</span></span>
<span data-ttu-id="fa2df-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fa2df-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa2df-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa2df-121">-WhatIf</span></span>
<span data-ttu-id="fa2df-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fa2df-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fa2df-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fa2df-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa2df-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa2df-124">CommonParameters</span></span>
<span data-ttu-id="fa2df-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fa2df-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa2df-126">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fa2df-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa2df-127">輸入</span><span class="sxs-lookup"><span data-stu-id="fa2df-127">INPUTS</span></span>

### <span data-ttu-id="fa2df-128">System.object</span><span class="sxs-lookup"><span data-stu-id="fa2df-128">System.String</span></span>

## <span data-ttu-id="fa2df-129">輸出</span><span class="sxs-lookup"><span data-stu-id="fa2df-129">OUTPUTS</span></span>

### <span data-ttu-id="fa2df-130">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="fa2df-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="fa2df-131">筆記</span><span class="sxs-lookup"><span data-stu-id="fa2df-131">NOTES</span></span>

## <span data-ttu-id="fa2df-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="fa2df-132">RELATED LINKS</span></span>
