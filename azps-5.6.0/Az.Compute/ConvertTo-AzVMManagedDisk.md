---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/convertto-azvmmanageddisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
ms.openlocfilehash: f73569e8e40af5111a738496ba6ad41ff03058f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906285"
---
# <span data-ttu-id="288db-101">ConvertTo-AzVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="288db-101">ConvertTo-AzVMManagedDisk</span></span>

## <span data-ttu-id="288db-102">簡介</span><span class="sxs-lookup"><span data-stu-id="288db-102">SYNOPSIS</span></span>
<span data-ttu-id="288db-103">將具有 Blob 型磁片的虛擬機器轉換為受管理磁片的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="288db-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

## <span data-ttu-id="288db-104">語法</span><span class="sxs-lookup"><span data-stu-id="288db-104">SYNTAX</span></span>

```
ConvertTo-AzVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="288db-105">描述</span><span class="sxs-lookup"><span data-stu-id="288db-105">DESCRIPTION</span></span>
<span data-ttu-id="288db-106">**ConvertTo-Az VIRTUALManagedObdlet Cmdlet** 會將具有 Blob 型磁片的虛擬機器轉換為具有受管理磁片的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="288db-106">The **ConvertTo-AzVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="288db-107">在重新執行此作業之前，必須先停止處理虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="288db-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="288db-108">例子</span><span class="sxs-lookup"><span data-stu-id="288db-108">EXAMPLES</span></span>

### <span data-ttu-id="288db-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="288db-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="288db-110">此命令會將資源群組 "ResourceGroup01" 中名為 "VM01" 的虛擬機器 Blob 型磁片轉換為受管理的磁片。</span><span class="sxs-lookup"><span data-stu-id="288db-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="288db-111">參數</span><span class="sxs-lookup"><span data-stu-id="288db-111">PARAMETERS</span></span>

### <span data-ttu-id="288db-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="288db-112">-AsJob</span></span>
<span data-ttu-id="288db-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="288db-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="288db-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="288db-114">-DefaultProfile</span></span>
<span data-ttu-id="288db-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="288db-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="288db-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="288db-116">-ResourceGroupName</span></span>
<span data-ttu-id="288db-117">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="288db-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="288db-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="288db-118">-VMName</span></span>
<span data-ttu-id="288db-119">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="288db-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="288db-120">-確認</span><span class="sxs-lookup"><span data-stu-id="288db-120">-Confirm</span></span>
<span data-ttu-id="288db-121">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="288db-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="288db-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="288db-122">-WhatIf</span></span>
<span data-ttu-id="288db-123">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="288db-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="288db-124">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="288db-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="288db-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="288db-125">CommonParameters</span></span>
<span data-ttu-id="288db-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="288db-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="288db-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="288db-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="288db-128">輸入</span><span class="sxs-lookup"><span data-stu-id="288db-128">INPUTS</span></span>

### <span data-ttu-id="288db-129">System.String</span><span class="sxs-lookup"><span data-stu-id="288db-129">System.String</span></span>

## <span data-ttu-id="288db-130">輸出</span><span class="sxs-lookup"><span data-stu-id="288db-130">OUTPUTS</span></span>

### <span data-ttu-id="288db-131">Microsoft.Azure.Commands.Compute.Automation.models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="288db-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="288db-132">筆記</span><span class="sxs-lookup"><span data-stu-id="288db-132">NOTES</span></span>

## <span data-ttu-id="288db-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="288db-133">RELATED LINKS</span></span>
