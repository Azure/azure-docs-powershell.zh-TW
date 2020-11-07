---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
ms.openlocfilehash: 8cd67aa715b0092c82a3553158a4736d8f1e850e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788521"
---
# <span data-ttu-id="dec8c-101">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="dec8c-101">Get-AzVMAEMExtension</span></span>

## <span data-ttu-id="dec8c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dec8c-102">SYNOPSIS</span></span>
<span data-ttu-id="dec8c-103">取得 AEM 延伸的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="dec8c-103">Gets information about the AEM extension.</span></span>

## <span data-ttu-id="dec8c-104">句法</span><span class="sxs-lookup"><span data-stu-id="dec8c-104">SYNTAX</span></span>

```
Get-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dec8c-105">說明</span><span class="sxs-lookup"><span data-stu-id="dec8c-105">DESCRIPTION</span></span>
<span data-ttu-id="dec8c-106">**AzVMAEMExtension** Cmdlet 會取得 Azure 增強型監視 (AEM) 延伸的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="dec8c-106">The **Get-AzVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="dec8c-107">示例</span><span class="sxs-lookup"><span data-stu-id="dec8c-107">EXAMPLES</span></span>

### <span data-ttu-id="dec8c-108">範例1：取得 AEM 延伸</span><span class="sxs-lookup"><span data-stu-id="dec8c-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="dec8c-109">這個命令會取得名為 contoso-server 的虛擬機器的 AEM 延伸資訊。</span><span class="sxs-lookup"><span data-stu-id="dec8c-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="dec8c-110">參數</span><span class="sxs-lookup"><span data-stu-id="dec8c-110">PARAMETERS</span></span>

### <span data-ttu-id="dec8c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dec8c-111">-DefaultProfile</span></span>
<span data-ttu-id="dec8c-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dec8c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dec8c-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="dec8c-113">-Name</span></span>
<span data-ttu-id="dec8c-114">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="dec8c-114">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="dec8c-115">這個 Cmdlet 會取得此 Cmdlet 所指定之虛擬機器上的 AEM 延伸資訊。</span><span class="sxs-lookup"><span data-stu-id="dec8c-115">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dec8c-116">-OSType</span><span class="sxs-lookup"><span data-stu-id="dec8c-116">-OSType</span></span>
<span data-ttu-id="dec8c-117">指定作業系統磁片作業系統的類型。</span><span class="sxs-lookup"><span data-stu-id="dec8c-117">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="dec8c-118">如果作業系統磁片沒有類型，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="dec8c-118">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="dec8c-119">此參數可接受的值為： Windows 和 Linux。</span><span class="sxs-lookup"><span data-stu-id="dec8c-119">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dec8c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dec8c-120">-ResourceGroupName</span></span>
<span data-ttu-id="dec8c-121">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dec8c-121">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="dec8c-122">這個 Cmdlet 會取得該虛擬機器上 AEM 延伸的資訊。</span><span class="sxs-lookup"><span data-stu-id="dec8c-122">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="dec8c-123">-狀態</span><span class="sxs-lookup"><span data-stu-id="dec8c-123">-Status</span></span>
<span data-ttu-id="dec8c-124">表示此 Cmdlet 只會取得 AEM 延伸的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="dec8c-124">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dec8c-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="dec8c-125">-VMName</span></span>
<span data-ttu-id="dec8c-126">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="dec8c-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="dec8c-127">這個 Cmdlet 會針對此參數指定的虛擬機器，取得 AEM 延伸的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="dec8c-127">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="dec8c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dec8c-128">CommonParameters</span></span>
<span data-ttu-id="dec8c-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dec8c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dec8c-130">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dec8c-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dec8c-131">輸入</span><span class="sxs-lookup"><span data-stu-id="dec8c-131">INPUTS</span></span>

### <span data-ttu-id="dec8c-132">System.object</span><span class="sxs-lookup"><span data-stu-id="dec8c-132">System.String</span></span>

### <span data-ttu-id="dec8c-133">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="dec8c-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dec8c-134">輸出</span><span class="sxs-lookup"><span data-stu-id="dec8c-134">OUTPUTS</span></span>

### <span data-ttu-id="dec8c-135">PSVirtualMachineExtension 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="dec8c-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="dec8c-136">筆記</span><span class="sxs-lookup"><span data-stu-id="dec8c-136">NOTES</span></span>

## <span data-ttu-id="dec8c-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="dec8c-137">RELATED LINKS</span></span>

[<span data-ttu-id="dec8c-138">移除-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="dec8c-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="dec8c-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="dec8c-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="dec8c-140">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="dec8c-140">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


