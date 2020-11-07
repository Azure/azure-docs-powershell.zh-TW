---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/test-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Test-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Test-AzVMAEMExtension.md
ms.openlocfilehash: 36fd9813523a5977c1981e6de54384cf71de7dc5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794828"
---
# <span data-ttu-id="5632c-101">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="5632c-101">Test-AzVMAEMExtension</span></span>

## <span data-ttu-id="5632c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5632c-102">SYNOPSIS</span></span>
<span data-ttu-id="5632c-103">檢查 AEM 延伸設定的設定。</span><span class="sxs-lookup"><span data-stu-id="5632c-103">Checks the configuration of the AEM extension.</span></span>

## <span data-ttu-id="5632c-104">句法</span><span class="sxs-lookup"><span data-stu-id="5632c-104">SYNTAX</span></span>

```
Test-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5632c-105">說明</span><span class="sxs-lookup"><span data-stu-id="5632c-105">DESCRIPTION</span></span>
<span data-ttu-id="5632c-106">**Test AzVMAEMExtension** Cmdlet 會檢查 Azure 增強型監視 (AEM) 延伸的設定。</span><span class="sxs-lookup"><span data-stu-id="5632c-106">The **Test-AzVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="5632c-107">AEM 延伸功能會收集效能資料。</span><span class="sxs-lookup"><span data-stu-id="5632c-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="5632c-108">這個 Cmdlet 會檢查是否有可用的效能資料。</span><span class="sxs-lookup"><span data-stu-id="5632c-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="5632c-109">示例</span><span class="sxs-lookup"><span data-stu-id="5632c-109">EXAMPLES</span></span>

### <span data-ttu-id="5632c-110">範例1：檢查 AEM 延伸設定的設定</span><span class="sxs-lookup"><span data-stu-id="5632c-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="5632c-111">這個命令會檢查名為 [contoso-伺服器] 的虛擬機器的 AEM 延伸設定。</span><span class="sxs-lookup"><span data-stu-id="5632c-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="5632c-112">參數</span><span class="sxs-lookup"><span data-stu-id="5632c-112">PARAMETERS</span></span>

### <span data-ttu-id="5632c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5632c-113">-DefaultProfile</span></span>
<span data-ttu-id="5632c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5632c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5632c-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="5632c-115">-OSType</span></span>
<span data-ttu-id="5632c-116">指定作業系統磁片作業系統的類型。</span><span class="sxs-lookup"><span data-stu-id="5632c-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="5632c-117">如果作業系統磁片沒有類型，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="5632c-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="5632c-118">此參數可接受的值為： Windows 和 Linux。</span><span class="sxs-lookup"><span data-stu-id="5632c-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="5632c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5632c-119">-ResourceGroupName</span></span>
<span data-ttu-id="5632c-120">指定此 Cmdlet 檢查之虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5632c-120">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="5632c-121">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="5632c-121">-SkipStorageCheck</span></span>
<span data-ttu-id="5632c-122">表示此 Cmdlet 會跳過儲存配置的檢查。</span><span class="sxs-lookup"><span data-stu-id="5632c-122">Indicates that this cmdlet skips the check of storage configuration.</span></span>

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

### <span data-ttu-id="5632c-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="5632c-123">-VMName</span></span>
<span data-ttu-id="5632c-124">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="5632c-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="5632c-125">這個 Cmdlet 會測試此參數指定之虛擬機器的 AEM 延伸。</span><span class="sxs-lookup"><span data-stu-id="5632c-125">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="5632c-126">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="5632c-126">-WaitTimeInMinutes</span></span>
<span data-ttu-id="5632c-127">指定儲存配置檢查的超時期間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="5632c-127">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

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

### <span data-ttu-id="5632c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5632c-128">CommonParameters</span></span>
<span data-ttu-id="5632c-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5632c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5632c-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5632c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5632c-131">輸入</span><span class="sxs-lookup"><span data-stu-id="5632c-131">INPUTS</span></span>

### <span data-ttu-id="5632c-132">所有</span><span class="sxs-lookup"><span data-stu-id="5632c-132">None</span></span>
<span data-ttu-id="5632c-133">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="5632c-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5632c-134">輸出</span><span class="sxs-lookup"><span data-stu-id="5632c-134">OUTPUTS</span></span>

### <span data-ttu-id="5632c-135">AEMTestResult 的計算副檔名. AEM</span><span class="sxs-lookup"><span data-stu-id="5632c-135">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span></span>

## <span data-ttu-id="5632c-136">筆記</span><span class="sxs-lookup"><span data-stu-id="5632c-136">NOTES</span></span>

## <span data-ttu-id="5632c-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="5632c-137">RELATED LINKS</span></span>

[<span data-ttu-id="5632c-138">AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="5632c-138">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="5632c-139">移除-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="5632c-139">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="5632c-140">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="5632c-140">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)


