---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVM.md
ms.openlocfilehash: 6fa67a039599ab066b82ad923f5a2f896b0db519
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625524"
---
# <span data-ttu-id="84c7b-101">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="84c7b-101">Set-AzureRmVM</span></span>

## <span data-ttu-id="84c7b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="84c7b-102">SYNOPSIS</span></span>
<span data-ttu-id="84c7b-103">將虛擬機器標示為「一般化」。</span><span class="sxs-lookup"><span data-stu-id="84c7b-103">Marks a virtual machine as generalized.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84c7b-104">句法</span><span class="sxs-lookup"><span data-stu-id="84c7b-104">SYNTAX</span></span>

### <span data-ttu-id="84c7b-105">GeneralizeResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="84c7b-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84c7b-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="84c7b-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84c7b-107">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="84c7b-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Generalized] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84c7b-108">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="84c7b-108">RedeployIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Redeploy] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="84c7b-109">說明</span><span class="sxs-lookup"><span data-stu-id="84c7b-109">DESCRIPTION</span></span>
<span data-ttu-id="84c7b-110">**AzureRmVM** Cmdlet 會將虛擬機器標示為「一般化」。</span><span class="sxs-lookup"><span data-stu-id="84c7b-110">The **Set-AzureRmVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="84c7b-111">在執行此 Cmdlet 之前，請先登入虛擬機器，然後使用 Sysprep 來準備硬碟。</span><span class="sxs-lookup"><span data-stu-id="84c7b-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="84c7b-112">示例</span><span class="sxs-lookup"><span data-stu-id="84c7b-112">EXAMPLES</span></span>

### <span data-ttu-id="84c7b-113">範例1：將虛擬機器標示為一般化</span><span class="sxs-lookup"><span data-stu-id="84c7b-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="84c7b-114">這個命令會將名為 VirtualMachine07 的虛擬機器標示為「一般化」。</span><span class="sxs-lookup"><span data-stu-id="84c7b-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="84c7b-115">參數</span><span class="sxs-lookup"><span data-stu-id="84c7b-115">PARAMETERS</span></span>

### <span data-ttu-id="84c7b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84c7b-116">-DefaultProfile</span></span>
<span data-ttu-id="84c7b-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="84c7b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84c7b-118">-通用化</span><span class="sxs-lookup"><span data-stu-id="84c7b-118">-Generalized</span></span>
<span data-ttu-id="84c7b-119">表示此 Cmdlet 會將虛擬機器標示為一般化。</span><span class="sxs-lookup"><span data-stu-id="84c7b-119">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, GeneralizeIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84c7b-120">-識別碼</span><span class="sxs-lookup"><span data-stu-id="84c7b-120">-Id</span></span>
<span data-ttu-id="84c7b-121">指定虛擬機器的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="84c7b-121">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84c7b-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="84c7b-122">-Name</span></span>
<span data-ttu-id="84c7b-123">指定此 Cmdlet 作用中的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="84c7b-123">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="84c7b-124">-重新部署</span><span class="sxs-lookup"><span data-stu-id="84c7b-124">-Redeploy</span></span>
<span data-ttu-id="84c7b-125">表示此 Cmdlet 會手動將虛擬機器 redeploys 至不同的 Azure 主機，以修正任何問題。</span><span class="sxs-lookup"><span data-stu-id="84c7b-125">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>

<span data-ttu-id="84c7b-126">如果您重新部署虛擬機器，它會重新開機，這會導致暫時的磁片磁碟機資料遺失。</span><span class="sxs-lookup"><span data-stu-id="84c7b-126">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84c7b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84c7b-127">-ResourceGroupName</span></span>
<span data-ttu-id="84c7b-128">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="84c7b-128">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84c7b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84c7b-129">CommonParameters</span></span>
<span data-ttu-id="84c7b-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="84c7b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84c7b-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="84c7b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84c7b-132">輸入</span><span class="sxs-lookup"><span data-stu-id="84c7b-132">INPUTS</span></span>

## <span data-ttu-id="84c7b-133">輸出</span><span class="sxs-lookup"><span data-stu-id="84c7b-133">OUTPUTS</span></span>

## <span data-ttu-id="84c7b-134">筆記</span><span class="sxs-lookup"><span data-stu-id="84c7b-134">NOTES</span></span>

## <span data-ttu-id="84c7b-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="84c7b-135">RELATED LINKS</span></span>

[<span data-ttu-id="84c7b-136">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="84c7b-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


