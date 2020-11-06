---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
ms.openlocfilehash: 343ecb5159b252c97af05cffc89152e05028583b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613251"
---
# <span data-ttu-id="e8834-101">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="e8834-101">Remove-AzVMAEMExtension</span></span>

## <span data-ttu-id="e8834-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8834-102">SYNOPSIS</span></span>
<span data-ttu-id="e8834-103">從虛擬機器中移除 AEM 延伸功能。</span><span class="sxs-lookup"><span data-stu-id="e8834-103">Removes the AEM extension from a virtual machine.</span></span>

## <span data-ttu-id="e8834-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8834-104">SYNTAX</span></span>

```
Remove-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8834-105">說明</span><span class="sxs-lookup"><span data-stu-id="e8834-105">DESCRIPTION</span></span>
<span data-ttu-id="e8834-106">**AzVMAEMExtension** Cmdlet 會將 Azure 增強型監視 (AEM) 延伸從虛擬機器中移除。</span><span class="sxs-lookup"><span data-stu-id="e8834-106">The **Remove-AzVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="e8834-107">示例</span><span class="sxs-lookup"><span data-stu-id="e8834-107">EXAMPLES</span></span>

### <span data-ttu-id="e8834-108">範例1：移除 AEM 延伸</span><span class="sxs-lookup"><span data-stu-id="e8834-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="e8834-109">這個命令會移除名為 contoso-server 的虛擬機器的 AEM 延伸功能。</span><span class="sxs-lookup"><span data-stu-id="e8834-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="e8834-110">參數</span><span class="sxs-lookup"><span data-stu-id="e8834-110">PARAMETERS</span></span>

### <span data-ttu-id="e8834-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8834-111">-DefaultProfile</span></span>
<span data-ttu-id="e8834-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8834-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8834-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8834-113">-Name</span></span>
<span data-ttu-id="e8834-114">指定此 Cmdlet 從中移除 AEM 延伸的虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8834-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="e8834-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e8834-115">-NoWait</span></span>
<span data-ttu-id="e8834-116">在作業完成之前，立即開始作業並立即返回。</span><span class="sxs-lookup"><span data-stu-id="e8834-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="e8834-117">若要判斷該作業是否已順利完成，請使用一些其他的機制。</span><span class="sxs-lookup"><span data-stu-id="e8834-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="e8834-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="e8834-118">-OSType</span></span>
<span data-ttu-id="e8834-119">指定作業系統磁片作業系統的類型。</span><span class="sxs-lookup"><span data-stu-id="e8834-119">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="e8834-120">如果作業系統磁片沒有類型，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="e8834-120">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="e8834-121">此參數可接受的值為： Windows 和 Linux。</span><span class="sxs-lookup"><span data-stu-id="e8834-121">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8834-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8834-122">-ResourceGroupName</span></span>
<span data-ttu-id="e8834-123">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8834-123">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="e8834-124">這個 Cmdlet 會從該虛擬機器中移除 AEM 延伸。</span><span class="sxs-lookup"><span data-stu-id="e8834-124">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="e8834-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="e8834-125">-VMName</span></span>
<span data-ttu-id="e8834-126">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8834-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="e8834-127">這個 Cmdlet 會移除此參數指定之虛擬機器的 AEM 延伸。</span><span class="sxs-lookup"><span data-stu-id="e8834-127">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="e8834-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8834-128">CommonParameters</span></span>
<span data-ttu-id="e8834-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8834-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8834-130">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e8834-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8834-131">輸入</span><span class="sxs-lookup"><span data-stu-id="e8834-131">INPUTS</span></span>

### <span data-ttu-id="e8834-132">System.object</span><span class="sxs-lookup"><span data-stu-id="e8834-132">System.String</span></span>

## <span data-ttu-id="e8834-133">輸出</span><span class="sxs-lookup"><span data-stu-id="e8834-133">OUTPUTS</span></span>

### <span data-ttu-id="e8834-134">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="e8834-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e8834-135">筆記</span><span class="sxs-lookup"><span data-stu-id="e8834-135">NOTES</span></span>

## <span data-ttu-id="e8834-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8834-136">RELATED LINKS</span></span>

[<span data-ttu-id="e8834-137">AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="e8834-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="e8834-138">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="e8834-138">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="e8834-139">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="e8834-139">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


