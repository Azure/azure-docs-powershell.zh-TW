---
external help file: AzureRM.Compute.ManagedService-help.xml
Module Name: AzureRM.Compute.ManagedService
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute.managedservice/convertto-azurermvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
ms.openlocfilehash: 0fa0f2d5cb78fe96f05b818b5cbfdabca47cbdee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445679"
---
# <span data-ttu-id="892d0-101">ConvertTo-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="892d0-101">ConvertTo-AzureRmVhd</span></span>

## <span data-ttu-id="892d0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="892d0-102">SYNOPSIS</span></span>
<span data-ttu-id="892d0-103">將 Hyper-v VM 轉換成 Azure 支援的虛擬硬碟檔案</span><span class="sxs-lookup"><span data-stu-id="892d0-103">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="892d0-104">句法</span><span class="sxs-lookup"><span data-stu-id="892d0-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVhd -HyperVVMName <String> -ExportPath <String> [-HyperVServer <String>] [-Force] [-AsJob]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="892d0-105">說明</span><span class="sxs-lookup"><span data-stu-id="892d0-105">DESCRIPTION</span></span>
<span data-ttu-id="892d0-106">將 Hyper-v VM 轉換成 Azure 支援的虛擬硬碟檔案</span><span class="sxs-lookup"><span data-stu-id="892d0-106">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

## <span data-ttu-id="892d0-107">示例</span><span class="sxs-lookup"><span data-stu-id="892d0-107">EXAMPLES</span></span>

### <span data-ttu-id="892d0-108">範例1</span><span class="sxs-lookup"><span data-stu-id="892d0-108">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVhd -HyperVVMName 'test' -ExportPath '.';
.\test\Virtual Hard Disks\Converted\os.vhd
.\test\Virtual Hard Disks\Converted\disk.vhd
```

<span data-ttu-id="892d0-109">將名為「test」的 Hyper-v VM 轉換為 Azure 支援的虛擬硬碟檔案至目前的資料夾。</span><span class="sxs-lookup"><span data-stu-id="892d0-109">Convert Hyper-V VM named 'test' to Azure supported virtual hard disk files to the current folder.</span></span>

## <span data-ttu-id="892d0-110">參數</span><span class="sxs-lookup"><span data-stu-id="892d0-110">PARAMETERS</span></span>

### <span data-ttu-id="892d0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="892d0-111">-AsJob</span></span>
<span data-ttu-id="892d0-112">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="892d0-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="892d0-113">-ExportPath</span><span class="sxs-lookup"><span data-stu-id="892d0-113">-ExportPath</span></span>
<span data-ttu-id="892d0-114">將包含磁片檔案的匯出資料夾路徑。</span><span class="sxs-lookup"><span data-stu-id="892d0-114">The export folder path that will contain the disk files.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="892d0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="892d0-115">-Force</span></span>
<span data-ttu-id="892d0-116">強制匯出，即使找到現有資料夾也一樣。</span><span class="sxs-lookup"><span data-stu-id="892d0-116">Force the export even if existing folder is found.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="892d0-117">-HyperVServer</span><span class="sxs-lookup"><span data-stu-id="892d0-117">-HyperVServer</span></span>
<span data-ttu-id="892d0-118">Hyper-v 伺服器 DNS 名稱，並以 "localhost" 做為預設值。</span><span class="sxs-lookup"><span data-stu-id="892d0-118">The Hyper-V server DNS name, with 'localhost' as the default value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="892d0-119">-HyperVVMName</span><span class="sxs-lookup"><span data-stu-id="892d0-119">-HyperVVMName</span></span>
<span data-ttu-id="892d0-120">Hyper-v 名稱名稱。</span><span class="sxs-lookup"><span data-stu-id="892d0-120">The Hyper-V name name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="892d0-121">-確認</span><span class="sxs-lookup"><span data-stu-id="892d0-121">-Confirm</span></span>
<span data-ttu-id="892d0-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="892d0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="892d0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="892d0-123">-WhatIf</span></span>
<span data-ttu-id="892d0-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="892d0-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="892d0-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="892d0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="892d0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="892d0-126">CommonParameters</span></span>
<span data-ttu-id="892d0-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="892d0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="892d0-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="892d0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="892d0-129">輸入</span><span class="sxs-lookup"><span data-stu-id="892d0-129">INPUTS</span></span>

### <span data-ttu-id="892d0-130">System.object</span><span class="sxs-lookup"><span data-stu-id="892d0-130">System.String</span></span>

## <span data-ttu-id="892d0-131">輸出</span><span class="sxs-lookup"><span data-stu-id="892d0-131">OUTPUTS</span></span>

### <span data-ttu-id="892d0-132">PathInfo 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="892d0-132">System.Management.Automation.PathInfo</span></span>

## <span data-ttu-id="892d0-133">筆記</span><span class="sxs-lookup"><span data-stu-id="892d0-133">NOTES</span></span>

## <span data-ttu-id="892d0-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="892d0-134">RELATED LINKS</span></span>
