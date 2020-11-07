---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
ms.openlocfilehash: ecda7c996bee6f707be27d3d58cf560ffaa50009
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794162"
---
# <span data-ttu-id="6bef2-101">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6bef2-101">Remove-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="6bef2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6bef2-102">SYNOPSIS</span></span>
<span data-ttu-id="6bef2-103">移除網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="6bef2-103">Removes a network security group.</span></span>

## <span data-ttu-id="6bef2-104">句法</span><span class="sxs-lookup"><span data-stu-id="6bef2-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bef2-105">說明</span><span class="sxs-lookup"><span data-stu-id="6bef2-105">DESCRIPTION</span></span>
<span data-ttu-id="6bef2-106">**AzNetworkSecurityGroup** Cmdlet 會移除 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="6bef2-106">The **Remove-AzNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="6bef2-107">示例</span><span class="sxs-lookup"><span data-stu-id="6bef2-107">EXAMPLES</span></span>

### <span data-ttu-id="6bef2-108">範例1：移除網路安全性群組</span><span class="sxs-lookup"><span data-stu-id="6bef2-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="6bef2-109">這個命令會在名為 TestRG 的資源群組中，移除名為 NSG-FrontEnd 的安全性群組。</span><span class="sxs-lookup"><span data-stu-id="6bef2-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="6bef2-110">參數</span><span class="sxs-lookup"><span data-stu-id="6bef2-110">PARAMETERS</span></span>

### <span data-ttu-id="6bef2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6bef2-111">-AsJob</span></span>
<span data-ttu-id="6bef2-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6bef2-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bef2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bef2-113">-DefaultProfile</span></span>
<span data-ttu-id="6bef2-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6bef2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6bef2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6bef2-115">-Force</span></span>
<span data-ttu-id="6bef2-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="6bef2-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bef2-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="6bef2-117">-Name</span></span>
<span data-ttu-id="6bef2-118">指定此 Cmdlet 移除之網路安全性群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6bef2-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bef2-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6bef2-119">-PassThru</span></span>
<span data-ttu-id="6bef2-120">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="6bef2-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6bef2-121">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="6bef2-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bef2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bef2-122">-ResourceGroupName</span></span>
<span data-ttu-id="6bef2-123">指定此 Cmdlet 移除網路安全群組的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6bef2-123">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bef2-124">-確認</span><span class="sxs-lookup"><span data-stu-id="6bef2-124">-Confirm</span></span>
<span data-ttu-id="6bef2-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6bef2-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bef2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bef2-126">-WhatIf</span></span>
<span data-ttu-id="6bef2-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6bef2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bef2-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6bef2-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bef2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bef2-129">CommonParameters</span></span>
<span data-ttu-id="6bef2-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6bef2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bef2-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6bef2-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bef2-132">輸入</span><span class="sxs-lookup"><span data-stu-id="6bef2-132">INPUTS</span></span>

## <span data-ttu-id="6bef2-133">輸出</span><span class="sxs-lookup"><span data-stu-id="6bef2-133">OUTPUTS</span></span>

## <span data-ttu-id="6bef2-134">筆記</span><span class="sxs-lookup"><span data-stu-id="6bef2-134">NOTES</span></span>

## <span data-ttu-id="6bef2-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="6bef2-135">RELATED LINKS</span></span>

[<span data-ttu-id="6bef2-136">AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6bef2-136">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="6bef2-137">新-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6bef2-137">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="6bef2-138">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6bef2-138">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


