---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: https://docs.microsoft.com/powershell/module/az.compute/test-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
ms.openlocfilehash: 040e7e557934fc90e5609a42c2e553ccf34d2f8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916773"
---
# <span data-ttu-id="92bb6-101">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="92bb6-101">Test-AzVMAEMExtension</span></span>

## <span data-ttu-id="92bb6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="92bb6-102">SYNOPSIS</span></span>
<span data-ttu-id="92bb6-103">檢查 AEM 擴充功能的配置。</span><span class="sxs-lookup"><span data-stu-id="92bb6-103">Checks the configuration of the AEM extension.</span></span>

## <span data-ttu-id="92bb6-104">語法</span><span class="sxs-lookup"><span data-stu-id="92bb6-104">SYNTAX</span></span>

```
Test-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="92bb6-105">描述</span><span class="sxs-lookup"><span data-stu-id="92bb6-105">DESCRIPTION</span></span>
<span data-ttu-id="92bb6-106">**Test-AzVMAEMExtension** Cmdlet 會檢查 Azure 增強型監控的 (AEM) 副檔名。</span><span class="sxs-lookup"><span data-stu-id="92bb6-106">The **Test-AzVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="92bb6-107">AEM 擴充功能會收集績效資料。</span><span class="sxs-lookup"><span data-stu-id="92bb6-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="92bb6-108">此 Cmdlet 會檢查是否提供績效資料。</span><span class="sxs-lookup"><span data-stu-id="92bb6-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="92bb6-109">例子</span><span class="sxs-lookup"><span data-stu-id="92bb6-109">EXAMPLES</span></span>

### <span data-ttu-id="92bb6-110">範例 1：檢查 AEM 擴充功能的配置</span><span class="sxs-lookup"><span data-stu-id="92bb6-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="92bb6-111">此命令會檢查名為 contoso-server 之虛擬機器的 AEM 擴充功能之組式。</span><span class="sxs-lookup"><span data-stu-id="92bb6-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="92bb6-112">參數</span><span class="sxs-lookup"><span data-stu-id="92bb6-112">PARAMETERS</span></span>

### <span data-ttu-id="92bb6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92bb6-113">-DefaultProfile</span></span>
<span data-ttu-id="92bb6-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="92bb6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92bb6-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="92bb6-115">-OSType</span></span>
<span data-ttu-id="92bb6-116">指定作業系統磁片的作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="92bb6-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="92bb6-117">如果作業系統磁片沒有類型，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="92bb6-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="92bb6-118">此參數可接受的值為：Windows 和 Linux。</span><span class="sxs-lookup"><span data-stu-id="92bb6-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92bb6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92bb6-119">-ResourceGroupName</span></span>
<span data-ttu-id="92bb6-120">指定此 Cmdlet 檢查之虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="92bb6-120">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="92bb6-121">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="92bb6-121">-SkipStorageCheck</span></span>
<span data-ttu-id="92bb6-122">表示此 Cmdlet 略過儲存空間配置的檢查。</span><span class="sxs-lookup"><span data-stu-id="92bb6-122">Indicates that this cmdlet skips the check of storage configuration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92bb6-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="92bb6-123">-VMName</span></span>
<span data-ttu-id="92bb6-124">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="92bb6-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="92bb6-125">此 Cmdlet 會測試此參數指定之虛擬機器的 AEM 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="92bb6-125">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92bb6-126">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="92bb6-126">-WaitTimeInMinutes</span></span>
<span data-ttu-id="92bb6-127">指定儲存設置檢查的時段 ，以分鐘為分。</span><span class="sxs-lookup"><span data-stu-id="92bb6-127">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

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

### <span data-ttu-id="92bb6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92bb6-128">CommonParameters</span></span>
<span data-ttu-id="92bb6-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="92bb6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92bb6-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92bb6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92bb6-131">輸入</span><span class="sxs-lookup"><span data-stu-id="92bb6-131">INPUTS</span></span>

### <span data-ttu-id="92bb6-132">System.String</span><span class="sxs-lookup"><span data-stu-id="92bb6-132">System.String</span></span>

## <span data-ttu-id="92bb6-133">輸出</span><span class="sxs-lookup"><span data-stu-id="92bb6-133">OUTPUTS</span></span>

### <span data-ttu-id="92bb6-134">Microsoft.Azure.Commands.Compute.extension.AEM.AEMTestResult</span><span class="sxs-lookup"><span data-stu-id="92bb6-134">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span></span>

## <span data-ttu-id="92bb6-135">筆記</span><span class="sxs-lookup"><span data-stu-id="92bb6-135">NOTES</span></span>

## <span data-ttu-id="92bb6-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="92bb6-136">RELATED LINKS</span></span>

[<span data-ttu-id="92bb6-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="92bb6-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="92bb6-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="92bb6-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="92bb6-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="92bb6-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)


