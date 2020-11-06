---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDscExtension.md
ms.openlocfilehash: d192d00be7de4561f8186671c17cca7328b0269f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445068"
---
# <span data-ttu-id="0d1d1-101">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="0d1d1-101">Remove-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="0d1d1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0d1d1-102">SYNOPSIS</span></span>
<span data-ttu-id="0d1d1-103">從資源群組中的虛擬機器移除 DSC 延伸處理常式。</span><span class="sxs-lookup"><span data-stu-id="0d1d1-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d1d1-104">句法</span><span class="sxs-lookup"><span data-stu-id="0d1d1-104">SYNTAX</span></span>

```
Remove-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d1d1-105">說明</span><span class="sxs-lookup"><span data-stu-id="0d1d1-105">DESCRIPTION</span></span>
<span data-ttu-id="0d1d1-106">**AzureRmVMDscExtension** Cmdlet 會從資源群組中的虛擬機器 (DSC) 延伸處理常式，移除所需的狀態設定。</span><span class="sxs-lookup"><span data-stu-id="0d1d1-106">The **Remove-AzureRmVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="0d1d1-107">示例</span><span class="sxs-lookup"><span data-stu-id="0d1d1-107">EXAMPLES</span></span>

### <span data-ttu-id="0d1d1-108">範例1：移除 DSC 副檔名</span><span class="sxs-lookup"><span data-stu-id="0d1d1-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzureRmVMDscExtension -ResouceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="0d1d1-109">這個命令會移除名為 VM07 的虛擬機器上名為 DSC 的延伸。</span><span class="sxs-lookup"><span data-stu-id="0d1d1-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="0d1d1-110">參數</span><span class="sxs-lookup"><span data-stu-id="0d1d1-110">PARAMETERS</span></span>

### <span data-ttu-id="0d1d1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d1d1-111">-DefaultProfile</span></span>
<span data-ttu-id="0d1d1-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0d1d1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1d1-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="0d1d1-113">-Name</span></span>
<span data-ttu-id="0d1d1-114">指定此 Cmdlet 移除的 DSC 副檔名名稱。</span><span class="sxs-lookup"><span data-stu-id="0d1d1-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="0d1d1-115">Set-AzureRmVMDscExtension Cmdlet 會將此名稱設定為 AzureRmVMDscExtension，這是 **Remove-** 所使用的預設值。</span><span class="sxs-lookup"><span data-stu-id="0d1d1-115">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzureRmVMDscExtension**.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d1d1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d1d1-116">-ResourceGroupName</span></span>
<span data-ttu-id="0d1d1-117">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d1d1-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0d1d1-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="0d1d1-118">-VMName</span></span>
<span data-ttu-id="0d1d1-119">指定此 Cmdlet 從中移除 DSC 副檔名的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="0d1d1-119">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d1d1-120">-確認</span><span class="sxs-lookup"><span data-stu-id="0d1d1-120">-Confirm</span></span>
<span data-ttu-id="0d1d1-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0d1d1-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1d1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d1d1-122">-WhatIf</span></span>
<span data-ttu-id="0d1d1-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0d1d1-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="0d1d1-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0d1d1-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1d1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d1d1-125">CommonParameters</span></span>
<span data-ttu-id="0d1d1-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0d1d1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d1d1-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0d1d1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d1d1-128">輸入</span><span class="sxs-lookup"><span data-stu-id="0d1d1-128">INPUTS</span></span>

## <span data-ttu-id="0d1d1-129">輸出</span><span class="sxs-lookup"><span data-stu-id="0d1d1-129">OUTPUTS</span></span>

## <span data-ttu-id="0d1d1-130">筆記</span><span class="sxs-lookup"><span data-stu-id="0d1d1-130">NOTES</span></span>

## <span data-ttu-id="0d1d1-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d1d1-131">RELATED LINKS</span></span>

[<span data-ttu-id="0d1d1-132">AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="0d1d1-132">Get-AzureRmVMDscExtension</span></span>](./Get-AzureRmVMDscExtension.md)

[<span data-ttu-id="0d1d1-133">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="0d1d1-133">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


