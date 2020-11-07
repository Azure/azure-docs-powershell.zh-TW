---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmss.md
ms.openlocfilehash: 22e281d7aa6e2d71506ddb616f96a149dcff6068
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796205"
---
# <span data-ttu-id="fce38-101">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fce38-101">Get-AzVmss</span></span>

## <span data-ttu-id="fce38-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fce38-102">SYNOPSIS</span></span>
<span data-ttu-id="fce38-103">取得 VMSS 的屬性。</span><span class="sxs-lookup"><span data-stu-id="fce38-103">Gets the properties of a VMSS.</span></span>

## <span data-ttu-id="fce38-104">句法</span><span class="sxs-lookup"><span data-stu-id="fce38-104">SYNTAX</span></span>

### <span data-ttu-id="fce38-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="fce38-105">DefaultParameter (Default)</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fce38-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="fce38-106">FriendMethod</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fce38-107">說明</span><span class="sxs-lookup"><span data-stu-id="fce38-107">DESCRIPTION</span></span>
<span data-ttu-id="fce38-108">**AzVmss** Cmdlet 會取得虛擬機器縮放集 (VMSS) 的模型和實例視圖。</span><span class="sxs-lookup"><span data-stu-id="fce38-108">The **Get-AzVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="fce38-109">模型視圖是使用者指定的虛擬機器屬性。</span><span class="sxs-lookup"><span data-stu-id="fce38-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="fce38-110">[實例] 視圖是虛擬機器的實例層級狀態。</span><span class="sxs-lookup"><span data-stu-id="fce38-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="fce38-111">指定 *Status* 參數，只取得虛擬機器的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="fce38-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="fce38-112">示例</span><span class="sxs-lookup"><span data-stu-id="fce38-112">EXAMPLES</span></span>

### <span data-ttu-id="fce38-113">範例1：取得 VMSS 的屬性</span><span class="sxs-lookup"><span data-stu-id="fce38-113">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="fce38-114">這個命令會取得屬於名為 Group001 之資源群組之名為 VMSS001 的 VMSS 屬性。</span><span class="sxs-lookup"><span data-stu-id="fce38-114">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="fce38-115">由於命令不會指定 *InstanceView* 切換參數，因此 Cmdlet 會取得虛擬機器的模型視圖。</span><span class="sxs-lookup"><span data-stu-id="fce38-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

## <span data-ttu-id="fce38-116">參數</span><span class="sxs-lookup"><span data-stu-id="fce38-116">PARAMETERS</span></span>

### <span data-ttu-id="fce38-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fce38-117">-DefaultProfile</span></span>
<span data-ttu-id="fce38-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fce38-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fce38-119">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="fce38-119">-InstanceView</span></span>
<span data-ttu-id="fce38-120">表示此 Cmdlet 只會取得虛擬機器的實例視圖。</span><span class="sxs-lookup"><span data-stu-id="fce38-120">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fce38-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fce38-121">-ResourceGroupName</span></span>
<span data-ttu-id="fce38-122">指定 VMSS 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fce38-122">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fce38-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="fce38-123">-VMScaleSetName</span></span>
<span data-ttu-id="fce38-124">Species VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="fce38-124">Species the name of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fce38-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fce38-125">CommonParameters</span></span>
<span data-ttu-id="fce38-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fce38-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fce38-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fce38-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fce38-128">輸入</span><span class="sxs-lookup"><span data-stu-id="fce38-128">INPUTS</span></span>

### <span data-ttu-id="fce38-129">所有</span><span class="sxs-lookup"><span data-stu-id="fce38-129">None</span></span>
<span data-ttu-id="fce38-130">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="fce38-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fce38-131">輸出</span><span class="sxs-lookup"><span data-stu-id="fce38-131">OUTPUTS</span></span>

### <span data-ttu-id="fce38-132">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="fce38-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="fce38-133">筆記</span><span class="sxs-lookup"><span data-stu-id="fce38-133">NOTES</span></span>

## <span data-ttu-id="fce38-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="fce38-134">RELATED LINKS</span></span>

[<span data-ttu-id="fce38-135">新-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fce38-135">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="fce38-136">移除-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fce38-136">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="fce38-137">重新開機-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fce38-137">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="fce38-138">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fce38-138">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="fce38-139">開始-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fce38-139">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="fce38-140">停止 AzVmss</span><span class="sxs-lookup"><span data-stu-id="fce38-140">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="fce38-141">更新-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fce38-141">Update-AzVmss</span></span>](./Update-AzVmss.md)


