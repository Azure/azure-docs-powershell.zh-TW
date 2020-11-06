---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVM.md
ms.openlocfilehash: f0d6ab84e457894b3c1ff7309efc6914350a03e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451732"
---
# <span data-ttu-id="93977-101">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="93977-101">Stop-AzureRmVM</span></span>

## <span data-ttu-id="93977-102">摘要</span><span class="sxs-lookup"><span data-stu-id="93977-102">SYNOPSIS</span></span>
<span data-ttu-id="93977-103">停止 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="93977-103">Stops an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93977-104">句法</span><span class="sxs-lookup"><span data-stu-id="93977-104">SYNTAX</span></span>

### <span data-ttu-id="93977-105">ResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="93977-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93977-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="93977-106">IdParameterSetName</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93977-107">說明</span><span class="sxs-lookup"><span data-stu-id="93977-107">DESCRIPTION</span></span>
<span data-ttu-id="93977-108">**AzureRmVM** Cmdlet 會停止 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="93977-108">The **Stop-AzureRmVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="93977-109">示例</span><span class="sxs-lookup"><span data-stu-id="93977-109">EXAMPLES</span></span>

### <span data-ttu-id="93977-110">範例1：停止虛擬機器</span><span class="sxs-lookup"><span data-stu-id="93977-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="93977-111">這個命令會在 ResourceGroup11 中停止名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="93977-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="93977-112">參數</span><span class="sxs-lookup"><span data-stu-id="93977-112">PARAMETERS</span></span>

### <span data-ttu-id="93977-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93977-113">-DefaultProfile</span></span>
<span data-ttu-id="93977-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="93977-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93977-115">-Force</span><span class="sxs-lookup"><span data-stu-id="93977-115">-Force</span></span>
<span data-ttu-id="93977-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="93977-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="93977-117">-識別碼</span><span class="sxs-lookup"><span data-stu-id="93977-117">-Id</span></span>
<span data-ttu-id="93977-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="93977-118">The resource group name.</span></span>

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

### <span data-ttu-id="93977-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="93977-119">-Name</span></span>
<span data-ttu-id="93977-120">虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="93977-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="93977-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93977-121">-ResourceGroupName</span></span>
<span data-ttu-id="93977-122">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="93977-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="93977-123">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="93977-123">-StayProvisioned</span></span>
<span data-ttu-id="93977-124">這個 Cmdlet 會停止 VMSS 中的所有虛擬機器，但不會解除配置。</span><span class="sxs-lookup"><span data-stu-id="93977-124">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="93977-125">帳戶會針對已停止的虛擬機器收取費用。</span><span class="sxs-lookup"><span data-stu-id="93977-125">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="93977-126">-確認</span><span class="sxs-lookup"><span data-stu-id="93977-126">-Confirm</span></span>
<span data-ttu-id="93977-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="93977-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93977-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93977-128">-WhatIf</span></span>
<span data-ttu-id="93977-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="93977-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="93977-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="93977-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93977-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93977-131">CommonParameters</span></span>
<span data-ttu-id="93977-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="93977-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93977-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="93977-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93977-134">輸入</span><span class="sxs-lookup"><span data-stu-id="93977-134">INPUTS</span></span>

## <span data-ttu-id="93977-135">輸出</span><span class="sxs-lookup"><span data-stu-id="93977-135">OUTPUTS</span></span>

## <span data-ttu-id="93977-136">筆記</span><span class="sxs-lookup"><span data-stu-id="93977-136">NOTES</span></span>

## <span data-ttu-id="93977-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="93977-137">RELATED LINKS</span></span>

[<span data-ttu-id="93977-138">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="93977-138">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="93977-139">新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="93977-139">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="93977-140">移除-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="93977-140">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="93977-141">重新開機-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="93977-141">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="93977-142">開始-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="93977-142">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="93977-143">更新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="93977-143">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


