---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
ms.openlocfilehash: 430c0d09c56aa4fb57399c97714dc70cb19dd500
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282851"
---
# <span data-ttu-id="705ae-101">New-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="705ae-101">New-AzDiskAccess</span></span>

## <span data-ttu-id="705ae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="705ae-102">SYNOPSIS</span></span>
<span data-ttu-id="705ae-103">建立磁片存取資源</span><span class="sxs-lookup"><span data-stu-id="705ae-103">Creates a Disk Access resource</span></span>

## <span data-ttu-id="705ae-104">句法</span><span class="sxs-lookup"><span data-stu-id="705ae-104">SYNTAX</span></span>

```
New-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="705ae-105">說明</span><span class="sxs-lookup"><span data-stu-id="705ae-105">DESCRIPTION</span></span>
<span data-ttu-id="705ae-106">**新的-AzDiskAccess** Cmdlet 會建立磁片存取資源</span><span class="sxs-lookup"><span data-stu-id="705ae-106">The **New-AzDiskAccess** cmdlet creates a Disk Access resource</span></span>

## <span data-ttu-id="705ae-107">示例</span><span class="sxs-lookup"><span data-stu-id="705ae-107">EXAMPLES</span></span>

### <span data-ttu-id="705ae-108">範例1</span><span class="sxs-lookup"><span data-stu-id="705ae-108">Example 1</span></span>
```
PS C:\> New-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" -Location "NorthCentralUS"
```

<span data-ttu-id="705ae-109">這個命令會以指定的屬性建立磁片存取。</span><span class="sxs-lookup"><span data-stu-id="705ae-109">This command will create a Disk Access with given properties.</span></span> 

## <span data-ttu-id="705ae-110">參數</span><span class="sxs-lookup"><span data-stu-id="705ae-110">PARAMETERS</span></span>

### <span data-ttu-id="705ae-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="705ae-111">-AsJob</span></span>
<span data-ttu-id="705ae-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="705ae-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="705ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="705ae-113">-DefaultProfile</span></span>
<span data-ttu-id="705ae-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="705ae-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="705ae-115">-位置</span><span class="sxs-lookup"><span data-stu-id="705ae-115">-Location</span></span>
<span data-ttu-id="705ae-116">指定位置。</span><span class="sxs-lookup"><span data-stu-id="705ae-116">Specifies the location.</span></span>

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

### <span data-ttu-id="705ae-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="705ae-117">-Name</span></span>
<span data-ttu-id="705ae-118">指定磁片存取的名稱。</span><span class="sxs-lookup"><span data-stu-id="705ae-118">Specifies the name of a disk access.</span></span>

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

### <span data-ttu-id="705ae-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="705ae-119">-ResourceGroupName</span></span>
<span data-ttu-id="705ae-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="705ae-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="705ae-121">-確認</span><span class="sxs-lookup"><span data-stu-id="705ae-121">-Confirm</span></span>
<span data-ttu-id="705ae-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="705ae-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="705ae-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="705ae-123">-WhatIf</span></span>
<span data-ttu-id="705ae-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="705ae-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="705ae-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="705ae-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="705ae-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="705ae-126">CommonParameters</span></span>
<span data-ttu-id="705ae-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="705ae-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="705ae-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="705ae-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="705ae-129">輸入</span><span class="sxs-lookup"><span data-stu-id="705ae-129">INPUTS</span></span>

### <span data-ttu-id="705ae-130">System.object</span><span class="sxs-lookup"><span data-stu-id="705ae-130">System.String</span></span>

## <span data-ttu-id="705ae-131">輸出</span><span class="sxs-lookup"><span data-stu-id="705ae-131">OUTPUTS</span></span>

### <span data-ttu-id="705ae-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="705ae-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="705ae-133">筆記</span><span class="sxs-lookup"><span data-stu-id="705ae-133">NOTES</span></span>

## <span data-ttu-id="705ae-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="705ae-134">RELATED LINKS</span></span>
