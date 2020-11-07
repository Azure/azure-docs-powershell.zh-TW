---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaemextension
schema: 2.0.0
ms.openlocfilehash: f5936a4be0170279d7416b05dc2b61fd22cfcca5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800554"
---
# <span data-ttu-id="1fa4b-101">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="1fa4b-101">Get-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="1fa4b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1fa4b-102">SYNOPSIS</span></span>
<span data-ttu-id="1fa4b-103">取得 AEM 延伸的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1fa4b-103">Gets information about the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fa4b-104">句法</span><span class="sxs-lookup"><span data-stu-id="1fa4b-104">SYNTAX</span></span>

```
Get-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fa4b-105">說明</span><span class="sxs-lookup"><span data-stu-id="1fa4b-105">DESCRIPTION</span></span>
<span data-ttu-id="1fa4b-106">**AzureRmVMAEMExtension** Cmdlet 會取得 Azure 增強型監視 (AEM) 延伸的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1fa4b-106">The **Get-AzureRmVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="1fa4b-107">示例</span><span class="sxs-lookup"><span data-stu-id="1fa4b-107">EXAMPLES</span></span>

### <span data-ttu-id="1fa4b-108">範例1：取得 AEM 延伸</span><span class="sxs-lookup"><span data-stu-id="1fa4b-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="1fa4b-109">這個命令會取得名為 contoso-server 的虛擬機器的 AEM 延伸資訊。</span><span class="sxs-lookup"><span data-stu-id="1fa4b-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="1fa4b-110">參數</span><span class="sxs-lookup"><span data-stu-id="1fa4b-110">PARAMETERS</span></span>

### <span data-ttu-id="1fa4b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fa4b-111">-DefaultProfile</span></span>
<span data-ttu-id="1fa4b-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1fa4b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fa4b-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="1fa4b-113">-Name</span></span>
<span data-ttu-id="1fa4b-114">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="1fa4b-114">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="1fa4b-115">這個 Cmdlet 會取得此 Cmdlet 所指定之虛擬機器上的 AEM 延伸資訊。</span><span class="sxs-lookup"><span data-stu-id="1fa4b-115">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="1fa4b-116">-OSType</span><span class="sxs-lookup"><span data-stu-id="1fa4b-116">-OSType</span></span>
<span data-ttu-id="1fa4b-117">指定作業系統磁片作業系統的類型。</span><span class="sxs-lookup"><span data-stu-id="1fa4b-117">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="1fa4b-118">如果作業系統磁片沒有類型，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="1fa4b-118">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="1fa4b-119">此參數可接受的值為： Windows 和 Linux。</span><span class="sxs-lookup"><span data-stu-id="1fa4b-119">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="1fa4b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fa4b-120">-ResourceGroupName</span></span>
<span data-ttu-id="1fa4b-121">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1fa4b-121">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="1fa4b-122">這個 Cmdlet 會取得該虛擬機器上 AEM 延伸的資訊。</span><span class="sxs-lookup"><span data-stu-id="1fa4b-122">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="1fa4b-123">-狀態</span><span class="sxs-lookup"><span data-stu-id="1fa4b-123">-Status</span></span>
<span data-ttu-id="1fa4b-124">表示此 Cmdlet 只會取得 AEM 延伸的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="1fa4b-124">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

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

### <span data-ttu-id="1fa4b-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="1fa4b-125">-VMName</span></span>
<span data-ttu-id="1fa4b-126">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="1fa4b-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="1fa4b-127">這個 Cmdlet 會針對此參數指定的虛擬機器，取得 AEM 延伸的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1fa4b-127">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="1fa4b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fa4b-128">CommonParameters</span></span>
<span data-ttu-id="1fa4b-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1fa4b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fa4b-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1fa4b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fa4b-131">輸入</span><span class="sxs-lookup"><span data-stu-id="1fa4b-131">INPUTS</span></span>

### <span data-ttu-id="1fa4b-132">所有</span><span class="sxs-lookup"><span data-stu-id="1fa4b-132">None</span></span>
<span data-ttu-id="1fa4b-133">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="1fa4b-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1fa4b-134">輸出</span><span class="sxs-lookup"><span data-stu-id="1fa4b-134">OUTPUTS</span></span>

### <span data-ttu-id="1fa4b-135">PSVirtualMachineExtension 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="1fa4b-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="1fa4b-136">筆記</span><span class="sxs-lookup"><span data-stu-id="1fa4b-136">NOTES</span></span>

## <span data-ttu-id="1fa4b-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="1fa4b-137">RELATED LINKS</span></span>

[<span data-ttu-id="1fa4b-138">移除-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="1fa4b-138">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="1fa4b-139">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="1fa4b-139">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="1fa4b-140">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="1fa4b-140">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


