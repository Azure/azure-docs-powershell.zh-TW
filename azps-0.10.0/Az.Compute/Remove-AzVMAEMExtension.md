---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
ms.openlocfilehash: 224d11aba6eece63c7c080415253b4833c665cee
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796069"
---
# <span data-ttu-id="6dd92-101">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="6dd92-101">Remove-AzVMAEMExtension</span></span>

## <span data-ttu-id="6dd92-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6dd92-102">SYNOPSIS</span></span>
<span data-ttu-id="6dd92-103">從虛擬機器中移除 AEM 延伸功能。</span><span class="sxs-lookup"><span data-stu-id="6dd92-103">Removes the AEM extension from a virtual machine.</span></span>

## <span data-ttu-id="6dd92-104">句法</span><span class="sxs-lookup"><span data-stu-id="6dd92-104">SYNTAX</span></span>

```
Remove-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6dd92-105">說明</span><span class="sxs-lookup"><span data-stu-id="6dd92-105">DESCRIPTION</span></span>
<span data-ttu-id="6dd92-106">**AzVMAEMExtension** Cmdlet 會將 Azure 增強型監視 (AEM) 延伸從虛擬機器中移除。</span><span class="sxs-lookup"><span data-stu-id="6dd92-106">The **Remove-AzVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="6dd92-107">示例</span><span class="sxs-lookup"><span data-stu-id="6dd92-107">EXAMPLES</span></span>

### <span data-ttu-id="6dd92-108">範例1：移除 AEM 延伸</span><span class="sxs-lookup"><span data-stu-id="6dd92-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="6dd92-109">這個命令會移除名為 contoso-server 的虛擬機器的 AEM 延伸功能。</span><span class="sxs-lookup"><span data-stu-id="6dd92-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="6dd92-110">參數</span><span class="sxs-lookup"><span data-stu-id="6dd92-110">PARAMETERS</span></span>

### <span data-ttu-id="6dd92-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dd92-111">-DefaultProfile</span></span>
<span data-ttu-id="6dd92-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6dd92-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6dd92-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="6dd92-113">-Name</span></span>
<span data-ttu-id="6dd92-114">指定此 Cmdlet 從中移除 AEM 延伸的虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="6dd92-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="6dd92-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="6dd92-115">-OSType</span></span>
<span data-ttu-id="6dd92-116">指定作業系統磁片作業系統的類型。</span><span class="sxs-lookup"><span data-stu-id="6dd92-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="6dd92-117">如果作業系統磁片沒有類型，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="6dd92-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="6dd92-118">此參數可接受的值為： Windows 和 Linux。</span><span class="sxs-lookup"><span data-stu-id="6dd92-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dd92-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dd92-119">-ResourceGroupName</span></span>
<span data-ttu-id="6dd92-120">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6dd92-120">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="6dd92-121">這個 Cmdlet 會從該虛擬機器中移除 AEM 延伸。</span><span class="sxs-lookup"><span data-stu-id="6dd92-121">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="6dd92-122">-VMName</span><span class="sxs-lookup"><span data-stu-id="6dd92-122">-VMName</span></span>
<span data-ttu-id="6dd92-123">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="6dd92-123">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="6dd92-124">這個 Cmdlet 會移除此參數指定之虛擬機器的 AEM 延伸。</span><span class="sxs-lookup"><span data-stu-id="6dd92-124">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="6dd92-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dd92-125">CommonParameters</span></span>
<span data-ttu-id="6dd92-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6dd92-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dd92-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6dd92-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dd92-128">輸入</span><span class="sxs-lookup"><span data-stu-id="6dd92-128">INPUTS</span></span>

### <span data-ttu-id="6dd92-129">所有</span><span class="sxs-lookup"><span data-stu-id="6dd92-129">None</span></span>
<span data-ttu-id="6dd92-130">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="6dd92-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6dd92-131">輸出</span><span class="sxs-lookup"><span data-stu-id="6dd92-131">OUTPUTS</span></span>

### <span data-ttu-id="6dd92-132">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="6dd92-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="6dd92-133">筆記</span><span class="sxs-lookup"><span data-stu-id="6dd92-133">NOTES</span></span>

## <span data-ttu-id="6dd92-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="6dd92-134">RELATED LINKS</span></span>

[<span data-ttu-id="6dd92-135">AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="6dd92-135">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="6dd92-136">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="6dd92-136">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="6dd92-137">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="6dd92-137">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


