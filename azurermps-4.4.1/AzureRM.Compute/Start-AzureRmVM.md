---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVM.md
ms.openlocfilehash: 3091cb877ff792527cf97e3d44b7c363f9dd94b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446875"
---
# <span data-ttu-id="e6eeb-101">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e6eeb-101">Start-AzureRmVM</span></span>

## <span data-ttu-id="e6eeb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e6eeb-102">SYNOPSIS</span></span>
<span data-ttu-id="e6eeb-103">啟動 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="e6eeb-103">Starts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6eeb-104">句法</span><span class="sxs-lookup"><span data-stu-id="e6eeb-104">SYNTAX</span></span>

### <span data-ttu-id="e6eeb-105">ResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="e6eeb-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzureRmVM [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6eeb-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e6eeb-106">IdParameterSetName</span></span>
```
Start-AzureRmVM [-Name] <String> [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e6eeb-107">說明</span><span class="sxs-lookup"><span data-stu-id="e6eeb-107">DESCRIPTION</span></span>
<span data-ttu-id="e6eeb-108">**AzureRmVM** Cmdlet 會啟動 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="e6eeb-108">The **Start-AzureRmVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="e6eeb-109">示例</span><span class="sxs-lookup"><span data-stu-id="e6eeb-109">EXAMPLES</span></span>

### <span data-ttu-id="e6eeb-110">範例1：啟動虛擬機器</span><span class="sxs-lookup"><span data-stu-id="e6eeb-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="e6eeb-111">這個命令會在 ResourceGroup11 中啟動名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="e6eeb-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="e6eeb-112">參數</span><span class="sxs-lookup"><span data-stu-id="e6eeb-112">PARAMETERS</span></span>

### <span data-ttu-id="e6eeb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6eeb-113">-DefaultProfile</span></span>
<span data-ttu-id="e6eeb-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e6eeb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6eeb-115">-識別碼</span><span class="sxs-lookup"><span data-stu-id="e6eeb-115">-Id</span></span>
<span data-ttu-id="e6eeb-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6eeb-116">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6eeb-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="e6eeb-117">-Name</span></span>
<span data-ttu-id="e6eeb-118">虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="e6eeb-118">The virtual machine name.</span></span>

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

### <span data-ttu-id="e6eeb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6eeb-119">-ResourceGroupName</span></span>
<span data-ttu-id="e6eeb-120">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6eeb-120">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6eeb-121">-確認</span><span class="sxs-lookup"><span data-stu-id="e6eeb-121">-Confirm</span></span>
<span data-ttu-id="e6eeb-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e6eeb-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6eeb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6eeb-123">-WhatIf</span></span>
<span data-ttu-id="e6eeb-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e6eeb-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6eeb-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e6eeb-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6eeb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6eeb-126">CommonParameters</span></span>
<span data-ttu-id="e6eeb-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e6eeb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6eeb-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e6eeb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6eeb-129">輸入</span><span class="sxs-lookup"><span data-stu-id="e6eeb-129">INPUTS</span></span>

## <span data-ttu-id="e6eeb-130">輸出</span><span class="sxs-lookup"><span data-stu-id="e6eeb-130">OUTPUTS</span></span>

## <span data-ttu-id="e6eeb-131">筆記</span><span class="sxs-lookup"><span data-stu-id="e6eeb-131">NOTES</span></span>

## <span data-ttu-id="e6eeb-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="e6eeb-132">RELATED LINKS</span></span>

[<span data-ttu-id="e6eeb-133">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e6eeb-133">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="e6eeb-134">新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e6eeb-134">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="e6eeb-135">移除-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e6eeb-135">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="e6eeb-136">重新開機-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e6eeb-136">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="e6eeb-137">停止 AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e6eeb-137">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="e6eeb-138">更新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e6eeb-138">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


