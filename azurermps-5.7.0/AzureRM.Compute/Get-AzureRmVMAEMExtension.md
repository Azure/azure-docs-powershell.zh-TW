---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
ms.openlocfilehash: 3970d26199fc122f248ad8e41a5146222cad23e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625928"
---
# <span data-ttu-id="2155f-101">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="2155f-101">Get-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="2155f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2155f-102">SYNOPSIS</span></span>
<span data-ttu-id="2155f-103">取得 AEM 延伸的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2155f-103">Gets information about the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2155f-104">句法</span><span class="sxs-lookup"><span data-stu-id="2155f-104">SYNTAX</span></span>

```
Get-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [<CommonParameters>]
```

## <span data-ttu-id="2155f-105">說明</span><span class="sxs-lookup"><span data-stu-id="2155f-105">DESCRIPTION</span></span>
<span data-ttu-id="2155f-106">**AzureRmVMAEMExtension** Cmdlet 會取得 Azure 增強型監視 (AEM) 延伸的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2155f-106">The **Get-AzureRmVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="2155f-107">示例</span><span class="sxs-lookup"><span data-stu-id="2155f-107">EXAMPLES</span></span>

### <span data-ttu-id="2155f-108">範例1：取得 AEM 延伸</span><span class="sxs-lookup"><span data-stu-id="2155f-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="2155f-109">這個命令會取得名為 contoso-server 的虛擬機器的 AEM 延伸資訊。</span><span class="sxs-lookup"><span data-stu-id="2155f-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="2155f-110">參數</span><span class="sxs-lookup"><span data-stu-id="2155f-110">PARAMETERS</span></span>

### <span data-ttu-id="2155f-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="2155f-111">-Name</span></span>
<span data-ttu-id="2155f-112">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="2155f-112">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="2155f-113">這個 Cmdlet 會取得此 Cmdlet 所指定之虛擬機器上的 AEM 延伸資訊。</span><span class="sxs-lookup"><span data-stu-id="2155f-113">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2155f-114">-OSType</span><span class="sxs-lookup"><span data-stu-id="2155f-114">-OSType</span></span>
<span data-ttu-id="2155f-115">指定作業系統磁片作業系統的類型。</span><span class="sxs-lookup"><span data-stu-id="2155f-115">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="2155f-116">如果作業系統磁片沒有類型，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="2155f-116">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="2155f-117">此參數可接受的值為： Windows 和 Linux。</span><span class="sxs-lookup"><span data-stu-id="2155f-117">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2155f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2155f-118">-ResourceGroupName</span></span>
<span data-ttu-id="2155f-119">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2155f-119">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="2155f-120">這個 Cmdlet 會取得該虛擬機器上 AEM 延伸的資訊。</span><span class="sxs-lookup"><span data-stu-id="2155f-120">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="2155f-121">-狀態</span><span class="sxs-lookup"><span data-stu-id="2155f-121">-Status</span></span>
<span data-ttu-id="2155f-122">表示此 Cmdlet 只會取得 AEM 延伸的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="2155f-122">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2155f-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="2155f-123">-VMName</span></span>
<span data-ttu-id="2155f-124">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="2155f-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="2155f-125">這個 Cmdlet 會針對此參數指定的虛擬機器，取得 AEM 延伸的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2155f-125">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="2155f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2155f-126">CommonParameters</span></span>
<span data-ttu-id="2155f-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2155f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2155f-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2155f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2155f-129">輸入</span><span class="sxs-lookup"><span data-stu-id="2155f-129">INPUTS</span></span>

### <span data-ttu-id="2155f-130">所有</span><span class="sxs-lookup"><span data-stu-id="2155f-130">None</span></span>
<span data-ttu-id="2155f-131">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="2155f-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2155f-132">輸出</span><span class="sxs-lookup"><span data-stu-id="2155f-132">OUTPUTS</span></span>

## <span data-ttu-id="2155f-133">筆記</span><span class="sxs-lookup"><span data-stu-id="2155f-133">NOTES</span></span>

## <span data-ttu-id="2155f-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="2155f-134">RELATED LINKS</span></span>

[<span data-ttu-id="2155f-135">移除-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="2155f-135">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="2155f-136">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="2155f-136">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="2155f-137">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="2155f-137">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


