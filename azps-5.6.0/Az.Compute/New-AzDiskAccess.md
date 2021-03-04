---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
ms.openlocfilehash: 430c0d09c56aa4fb57399c97714dc70cb19dd500
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909145"
---
# <span data-ttu-id="fea31-101">New-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="fea31-101">New-AzDiskAccess</span></span>

## <span data-ttu-id="fea31-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fea31-102">SYNOPSIS</span></span>
<span data-ttu-id="fea31-103">建立磁片存取資源</span><span class="sxs-lookup"><span data-stu-id="fea31-103">Creates a Disk Access resource</span></span>

## <span data-ttu-id="fea31-104">語法</span><span class="sxs-lookup"><span data-stu-id="fea31-104">SYNTAX</span></span>

```
New-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fea31-105">描述</span><span class="sxs-lookup"><span data-stu-id="fea31-105">DESCRIPTION</span></span>
<span data-ttu-id="fea31-106">**New-Az在Access** Cmdlet 中建立磁片存取資源</span><span class="sxs-lookup"><span data-stu-id="fea31-106">The **New-AzDiskAccess** cmdlet creates a Disk Access resource</span></span>

## <span data-ttu-id="fea31-107">例子</span><span class="sxs-lookup"><span data-stu-id="fea31-107">EXAMPLES</span></span>

### <span data-ttu-id="fea31-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="fea31-108">Example 1</span></span>
```
PS C:\> New-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" -Location "NorthCentralUS"
```

<span data-ttu-id="fea31-109">此命令會建立具有指定屬性的磁片存取。</span><span class="sxs-lookup"><span data-stu-id="fea31-109">This command will create a Disk Access with given properties.</span></span> 

## <span data-ttu-id="fea31-110">參數</span><span class="sxs-lookup"><span data-stu-id="fea31-110">PARAMETERS</span></span>

### <span data-ttu-id="fea31-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fea31-111">-AsJob</span></span>
<span data-ttu-id="fea31-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fea31-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fea31-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fea31-113">-DefaultProfile</span></span>
<span data-ttu-id="fea31-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fea31-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fea31-115">-位置</span><span class="sxs-lookup"><span data-stu-id="fea31-115">-Location</span></span>
<span data-ttu-id="fea31-116">指定位置。</span><span class="sxs-lookup"><span data-stu-id="fea31-116">Specifies the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fea31-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="fea31-117">-Name</span></span>
<span data-ttu-id="fea31-118">指定磁片存取的名稱。</span><span class="sxs-lookup"><span data-stu-id="fea31-118">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskAccessName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fea31-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fea31-119">-ResourceGroupName</span></span>
<span data-ttu-id="fea31-120">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fea31-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="fea31-121">-確認</span><span class="sxs-lookup"><span data-stu-id="fea31-121">-Confirm</span></span>
<span data-ttu-id="fea31-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="fea31-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fea31-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fea31-123">-WhatIf</span></span>
<span data-ttu-id="fea31-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fea31-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fea31-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fea31-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fea31-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fea31-126">CommonParameters</span></span>
<span data-ttu-id="fea31-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fea31-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fea31-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fea31-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fea31-129">輸入</span><span class="sxs-lookup"><span data-stu-id="fea31-129">INPUTS</span></span>

### <span data-ttu-id="fea31-130">System.String</span><span class="sxs-lookup"><span data-stu-id="fea31-130">System.String</span></span>

## <span data-ttu-id="fea31-131">輸出</span><span class="sxs-lookup"><span data-stu-id="fea31-131">OUTPUTS</span></span>

### <span data-ttu-id="fea31-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="fea31-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="fea31-133">筆記</span><span class="sxs-lookup"><span data-stu-id="fea31-133">NOTES</span></span>

## <span data-ttu-id="fea31-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="fea31-134">RELATED LINKS</span></span>
