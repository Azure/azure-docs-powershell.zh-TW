---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Test-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Test-AzureRmVMAEMExtension.md
ms.openlocfilehash: d766102b0e87968e59bdd9bf63157dd62e977a25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444683"
---
# <span data-ttu-id="29ef4-101">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="29ef4-101">Test-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="29ef4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="29ef4-102">SYNOPSIS</span></span>
<span data-ttu-id="29ef4-103">檢查 AEM 延伸設定的設定。</span><span class="sxs-lookup"><span data-stu-id="29ef4-103">Checks the configuration of the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29ef4-104">句法</span><span class="sxs-lookup"><span data-stu-id="29ef4-104">SYNTAX</span></span>

```
Test-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [<CommonParameters>]
```

## <span data-ttu-id="29ef4-105">說明</span><span class="sxs-lookup"><span data-stu-id="29ef4-105">DESCRIPTION</span></span>
<span data-ttu-id="29ef4-106">**Test AzureRmVMAEMExtension** Cmdlet 會檢查 Azure 增強型監視 (AEM) 延伸的設定。</span><span class="sxs-lookup"><span data-stu-id="29ef4-106">The **Test-AzureRmVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="29ef4-107">AEM 延伸功能會收集效能資料。</span><span class="sxs-lookup"><span data-stu-id="29ef4-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="29ef4-108">這個 Cmdlet 會檢查是否有可用的效能資料。</span><span class="sxs-lookup"><span data-stu-id="29ef4-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="29ef4-109">示例</span><span class="sxs-lookup"><span data-stu-id="29ef4-109">EXAMPLES</span></span>

### <span data-ttu-id="29ef4-110">範例1：檢查 AEM 延伸設定的設定</span><span class="sxs-lookup"><span data-stu-id="29ef4-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="29ef4-111">這個命令會檢查名為 [contoso-伺服器] 的虛擬機器的 AEM 延伸設定。</span><span class="sxs-lookup"><span data-stu-id="29ef4-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="29ef4-112">參數</span><span class="sxs-lookup"><span data-stu-id="29ef4-112">PARAMETERS</span></span>

### <span data-ttu-id="29ef4-113">-OSType</span><span class="sxs-lookup"><span data-stu-id="29ef4-113">-OSType</span></span>
<span data-ttu-id="29ef4-114">指定作業系統磁片作業系統的類型。</span><span class="sxs-lookup"><span data-stu-id="29ef4-114">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="29ef4-115">如果作業系統磁片沒有類型，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="29ef4-115">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="29ef4-116">此參數可接受的值為： Windows 和 Linux。</span><span class="sxs-lookup"><span data-stu-id="29ef4-116">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29ef4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29ef4-117">-ResourceGroupName</span></span>
<span data-ttu-id="29ef4-118">指定此 Cmdlet 檢查之虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="29ef4-118">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29ef4-119">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="29ef4-119">-SkipStorageCheck</span></span>
<span data-ttu-id="29ef4-120">表示此 Cmdlet 會跳過儲存配置的檢查。</span><span class="sxs-lookup"><span data-stu-id="29ef4-120">Indicates that this cmdlet skips the check of storage configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29ef4-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="29ef4-121">-VMName</span></span>
<span data-ttu-id="29ef4-122">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="29ef4-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="29ef4-123">這個 Cmdlet 會測試此參數指定之虛擬機器的 AEM 延伸。</span><span class="sxs-lookup"><span data-stu-id="29ef4-123">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29ef4-124">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="29ef4-124">-WaitTimeInMinutes</span></span>
<span data-ttu-id="29ef4-125">指定儲存配置檢查的超時期間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="29ef4-125">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29ef4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29ef4-126">CommonParameters</span></span>
<span data-ttu-id="29ef4-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="29ef4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29ef4-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="29ef4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29ef4-129">輸入</span><span class="sxs-lookup"><span data-stu-id="29ef4-129">INPUTS</span></span>

### <span data-ttu-id="29ef4-130">所有</span><span class="sxs-lookup"><span data-stu-id="29ef4-130">None</span></span>
<span data-ttu-id="29ef4-131">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="29ef4-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="29ef4-132">輸出</span><span class="sxs-lookup"><span data-stu-id="29ef4-132">OUTPUTS</span></span>

## <span data-ttu-id="29ef4-133">筆記</span><span class="sxs-lookup"><span data-stu-id="29ef4-133">NOTES</span></span>

## <span data-ttu-id="29ef4-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="29ef4-134">RELATED LINKS</span></span>

[<span data-ttu-id="29ef4-135">AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="29ef4-135">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="29ef4-136">移除-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="29ef4-136">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="29ef4-137">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="29ef4-137">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)


