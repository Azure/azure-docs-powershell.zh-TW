---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/grant-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
ms.openlocfilehash: 709fab1ab8ba39193ef9831cd03d7b1cd53208dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914897"
---
# <span data-ttu-id="eff9f-101">Grant-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="eff9f-101">Grant-AzDiskAccess</span></span>

## <span data-ttu-id="eff9f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eff9f-102">SYNOPSIS</span></span>
<span data-ttu-id="eff9f-103">授予磁片的存取權。</span><span class="sxs-lookup"><span data-stu-id="eff9f-103">Grants an access to a disk.</span></span>

## <span data-ttu-id="eff9f-104">語法</span><span class="sxs-lookup"><span data-stu-id="eff9f-104">SYNTAX</span></span>

```
Grant-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eff9f-105">描述</span><span class="sxs-lookup"><span data-stu-id="eff9f-105">DESCRIPTION</span></span>
<span data-ttu-id="eff9f-106">**Grant-Az與Access** Cmdlet 會授予磁片的存取權。</span><span class="sxs-lookup"><span data-stu-id="eff9f-106">The **Grant-AzDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="eff9f-107">例子</span><span class="sxs-lookup"><span data-stu-id="eff9f-107">EXAMPLES</span></span>

### <span data-ttu-id="eff9f-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="eff9f-108">Example 1</span></span>
```
PS C:\> Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="eff9f-109">將名為 'ResourceGroup01' 的資源群組中名為 "Disk01" 的磁片的讀取存取權授予 60 秒。</span><span class="sxs-lookup"><span data-stu-id="eff9f-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="eff9f-110">參數</span><span class="sxs-lookup"><span data-stu-id="eff9f-110">PARAMETERS</span></span>

### <span data-ttu-id="eff9f-111">-Access</span><span class="sxs-lookup"><span data-stu-id="eff9f-111">-Access</span></span>
<span data-ttu-id="eff9f-112">指定 Access 層級。</span><span class="sxs-lookup"><span data-stu-id="eff9f-112">Specifies Access level.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eff9f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eff9f-113">-AsJob</span></span>
<span data-ttu-id="eff9f-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eff9f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eff9f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eff9f-115">-DefaultProfile</span></span>
<span data-ttu-id="eff9f-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="eff9f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eff9f-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="eff9f-117">-DiskName</span></span>
<span data-ttu-id="eff9f-118">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="eff9f-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="eff9f-119">-DurationIn用</span><span class="sxs-lookup"><span data-stu-id="eff9f-119">-DurationInSecond</span></span>
<span data-ttu-id="eff9f-120">以秒數指定存取持續時間。</span><span class="sxs-lookup"><span data-stu-id="eff9f-120">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eff9f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eff9f-121">-ResourceGroupName</span></span>
<span data-ttu-id="eff9f-122">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="eff9f-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="eff9f-123">-確認</span><span class="sxs-lookup"><span data-stu-id="eff9f-123">-Confirm</span></span>
<span data-ttu-id="eff9f-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="eff9f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eff9f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eff9f-125">-WhatIf</span></span>
<span data-ttu-id="eff9f-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eff9f-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eff9f-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eff9f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eff9f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eff9f-128">CommonParameters</span></span>
<span data-ttu-id="eff9f-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eff9f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eff9f-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eff9f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eff9f-131">輸入</span><span class="sxs-lookup"><span data-stu-id="eff9f-131">INPUTS</span></span>

### <span data-ttu-id="eff9f-132">System.String</span><span class="sxs-lookup"><span data-stu-id="eff9f-132">System.String</span></span>

## <span data-ttu-id="eff9f-133">輸出</span><span class="sxs-lookup"><span data-stu-id="eff9f-133">OUTPUTS</span></span>

### <span data-ttu-id="eff9f-134">Microsoft.Azure.Commands.Compute.Automation.models.PSAccesssUri</span><span class="sxs-lookup"><span data-stu-id="eff9f-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="eff9f-135">筆記</span><span class="sxs-lookup"><span data-stu-id="eff9f-135">NOTES</span></span>

## <span data-ttu-id="eff9f-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="eff9f-136">RELATED LINKS</span></span>
