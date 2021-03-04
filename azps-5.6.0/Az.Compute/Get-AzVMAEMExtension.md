---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
ms.openlocfilehash: ed5f79763d8e9786f0a502f404474eeef2f641f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903670"
---
# <span data-ttu-id="4564e-101">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="4564e-101">Get-AzVMAEMExtension</span></span>

## <span data-ttu-id="4564e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4564e-102">SYNOPSIS</span></span>
<span data-ttu-id="4564e-103">獲得 AEM 擴充功能的資訊。</span><span class="sxs-lookup"><span data-stu-id="4564e-103">Gets information about the AEM extension.</span></span>

## <span data-ttu-id="4564e-104">語法</span><span class="sxs-lookup"><span data-stu-id="4564e-104">SYNTAX</span></span>

```
Get-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4564e-105">描述</span><span class="sxs-lookup"><span data-stu-id="4564e-105">DESCRIPTION</span></span>
<span data-ttu-id="4564e-106">**Get-AzVMAEMExtension** Cmdlet 會取得有關 Azure 增強型監控 (AEM) 副檔名。</span><span class="sxs-lookup"><span data-stu-id="4564e-106">The **Get-AzVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="4564e-107">例子</span><span class="sxs-lookup"><span data-stu-id="4564e-107">EXAMPLES</span></span>

### <span data-ttu-id="4564e-108">範例 1：取得 AEM 擴充功能</span><span class="sxs-lookup"><span data-stu-id="4564e-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="4564e-109">此命令會針對名為 contoso-server 的虛擬機器，獲得 AEM 擴充功能的資訊。</span><span class="sxs-lookup"><span data-stu-id="4564e-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="4564e-110">參數</span><span class="sxs-lookup"><span data-stu-id="4564e-110">PARAMETERS</span></span>

### <span data-ttu-id="4564e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4564e-111">-DefaultProfile</span></span>
<span data-ttu-id="4564e-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4564e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4564e-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="4564e-113">-Name</span></span>
<span data-ttu-id="4564e-114">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="4564e-114">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="4564e-115">此 Cmdlet 會在此 Cmdlet 指定的虛擬機器上，獲得 AEM 擴充功能的資訊。</span><span class="sxs-lookup"><span data-stu-id="4564e-115">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="4564e-116">-OSType</span><span class="sxs-lookup"><span data-stu-id="4564e-116">-OSType</span></span>
<span data-ttu-id="4564e-117">指定作業系統磁片的作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="4564e-117">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="4564e-118">如果作業系統磁片沒有類型，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="4564e-118">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="4564e-119">此參數可接受的值為：Windows 和 Linux。</span><span class="sxs-lookup"><span data-stu-id="4564e-119">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="4564e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4564e-120">-ResourceGroupName</span></span>
<span data-ttu-id="4564e-121">指定虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="4564e-121">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="4564e-122">此 Cmdlet 會獲得該虛擬機器上 AEM 擴充功能的資訊。</span><span class="sxs-lookup"><span data-stu-id="4564e-122">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="4564e-123">-狀態</span><span class="sxs-lookup"><span data-stu-id="4564e-123">-Status</span></span>
<span data-ttu-id="4564e-124">表示此 Cmdlet 僅會獲得 AEM 擴充功能的實例視圖。</span><span class="sxs-lookup"><span data-stu-id="4564e-124">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

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

### <span data-ttu-id="4564e-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="4564e-125">-VMName</span></span>
<span data-ttu-id="4564e-126">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="4564e-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="4564e-127">此 Cmdlet 會針對此參數指定的虛擬機器，獲得 AEM 擴充功能的資訊。</span><span class="sxs-lookup"><span data-stu-id="4564e-127">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="4564e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4564e-128">CommonParameters</span></span>
<span data-ttu-id="4564e-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4564e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4564e-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4564e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4564e-131">輸入</span><span class="sxs-lookup"><span data-stu-id="4564e-131">INPUTS</span></span>

### <span data-ttu-id="4564e-132">System.String</span><span class="sxs-lookup"><span data-stu-id="4564e-132">System.String</span></span>

### <span data-ttu-id="4564e-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4564e-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4564e-134">輸出</span><span class="sxs-lookup"><span data-stu-id="4564e-134">OUTPUTS</span></span>

### <span data-ttu-id="4564e-135">Microsoft.Azure.Commands.Compute.models.PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="4564e-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="4564e-136">筆記</span><span class="sxs-lookup"><span data-stu-id="4564e-136">NOTES</span></span>

## <span data-ttu-id="4564e-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="4564e-137">RELATED LINKS</span></span>

[<span data-ttu-id="4564e-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="4564e-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="4564e-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="4564e-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="4564e-140">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="4564e-140">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


