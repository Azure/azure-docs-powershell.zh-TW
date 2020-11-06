---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMExtension.md
ms.openlocfilehash: 164fdd36ca0e97dde33caec1322ddfa2bb6a15c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445067"
---
# <span data-ttu-id="2cbd3-101">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="2cbd3-101">Remove-AzureRmVMExtension</span></span>

## <span data-ttu-id="2cbd3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2cbd3-102">SYNOPSIS</span></span>
<span data-ttu-id="2cbd3-103">從虛擬機器移除延伸。</span><span class="sxs-lookup"><span data-stu-id="2cbd3-103">Removes an extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cbd3-104">句法</span><span class="sxs-lookup"><span data-stu-id="2cbd3-104">SYNTAX</span></span>

```
Remove-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cbd3-105">說明</span><span class="sxs-lookup"><span data-stu-id="2cbd3-105">DESCRIPTION</span></span>
<span data-ttu-id="2cbd3-106">**AzureRmVMExtension** Cmdlet 會從虛擬機器的虛擬機器延伸中移除延伸。</span><span class="sxs-lookup"><span data-stu-id="2cbd3-106">The **Remove-AzureRmVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="2cbd3-107">示例</span><span class="sxs-lookup"><span data-stu-id="2cbd3-107">EXAMPLES</span></span>

### <span data-ttu-id="2cbd3-108">範例1：從虛擬機器移除擴充功能</span><span class="sxs-lookup"><span data-stu-id="2cbd3-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="2cbd3-109">這個命令會從 ResourceGroup11 中名為 VirtualMachine22 的虛擬機器中移除名為 ContosoTest 的延伸。</span><span class="sxs-lookup"><span data-stu-id="2cbd3-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="2cbd3-110">參數</span><span class="sxs-lookup"><span data-stu-id="2cbd3-110">PARAMETERS</span></span>

### <span data-ttu-id="2cbd3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cbd3-111">-DefaultProfile</span></span>
<span data-ttu-id="2cbd3-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2cbd3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cbd3-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2cbd3-113">-Force</span></span>
<span data-ttu-id="2cbd3-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="2cbd3-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2cbd3-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="2cbd3-115">-Name</span></span>
<span data-ttu-id="2cbd3-116">指定此 Cmdlet 移除的延伸名稱。</span><span class="sxs-lookup"><span data-stu-id="2cbd3-116">Specifies the name of the extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cbd3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cbd3-117">-ResourceGroupName</span></span>
<span data-ttu-id="2cbd3-118">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2cbd3-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="2cbd3-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="2cbd3-119">-VMName</span></span>
<span data-ttu-id="2cbd3-120">指定此 Cmdlet 從中移除延伸的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="2cbd3-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="2cbd3-121">-確認</span><span class="sxs-lookup"><span data-stu-id="2cbd3-121">-Confirm</span></span>
<span data-ttu-id="2cbd3-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2cbd3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cbd3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cbd3-123">-WhatIf</span></span>
<span data-ttu-id="2cbd3-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2cbd3-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="2cbd3-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2cbd3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cbd3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cbd3-126">CommonParameters</span></span>
<span data-ttu-id="2cbd3-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2cbd3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cbd3-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2cbd3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cbd3-129">輸入</span><span class="sxs-lookup"><span data-stu-id="2cbd3-129">INPUTS</span></span>

## <span data-ttu-id="2cbd3-130">輸出</span><span class="sxs-lookup"><span data-stu-id="2cbd3-130">OUTPUTS</span></span>

## <span data-ttu-id="2cbd3-131">筆記</span><span class="sxs-lookup"><span data-stu-id="2cbd3-131">NOTES</span></span>

## <span data-ttu-id="2cbd3-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="2cbd3-132">RELATED LINKS</span></span>

[<span data-ttu-id="2cbd3-133">AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="2cbd3-133">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="2cbd3-134">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="2cbd3-134">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


