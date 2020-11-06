---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterface.md
ms.openlocfilehash: 829dc03dad037b6b1576613ab18d9929a777241e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446176"
---
# <span data-ttu-id="758b4-101">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="758b4-101">Remove-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="758b4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="758b4-102">SYNOPSIS</span></span>
<span data-ttu-id="758b4-103">移除網路介面。</span><span class="sxs-lookup"><span data-stu-id="758b4-103">Removes a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="758b4-104">句法</span><span class="sxs-lookup"><span data-stu-id="758b4-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="758b4-105">說明</span><span class="sxs-lookup"><span data-stu-id="758b4-105">DESCRIPTION</span></span>
<span data-ttu-id="758b4-106">**AzureRmNetworkInterface** Cmdlet 會移除 Azure 網路介面。</span><span class="sxs-lookup"><span data-stu-id="758b4-106">The **Remove-AzureRmNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="758b4-107">示例</span><span class="sxs-lookup"><span data-stu-id="758b4-107">EXAMPLES</span></span>

### <span data-ttu-id="758b4-108">範例1：移除網路介面</span><span class="sxs-lookup"><span data-stu-id="758b4-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="758b4-109">這個命令會移除 [資源群組 ResourceGroup1] 中的 [網路介面 NetworkInterface1]。</span><span class="sxs-lookup"><span data-stu-id="758b4-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="758b4-110">由於不使用 *Force* 參數，系統會提示使用者確認此動作。</span><span class="sxs-lookup"><span data-stu-id="758b4-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="758b4-111">範例2：移除網路介面</span><span class="sxs-lookup"><span data-stu-id="758b4-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzureRmNetworkInterface -Force
```

<span data-ttu-id="758b4-112">這個命令會移除 [資源群組 ResourceGroup1] 中的所有網路介面。</span><span class="sxs-lookup"><span data-stu-id="758b4-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="758b4-113">因為使用 *Force* 參數，系統不會提示使用者確認。</span><span class="sxs-lookup"><span data-stu-id="758b4-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="758b4-114">參數</span><span class="sxs-lookup"><span data-stu-id="758b4-114">PARAMETERS</span></span>

### <span data-ttu-id="758b4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="758b4-115">-AsJob</span></span>
<span data-ttu-id="758b4-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="758b4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="758b4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="758b4-117">-DefaultProfile</span></span>
<span data-ttu-id="758b4-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="758b4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="758b4-119">-Force</span><span class="sxs-lookup"><span data-stu-id="758b4-119">-Force</span></span>
<span data-ttu-id="758b4-120">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="758b4-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="758b4-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="758b4-121">-Name</span></span>
<span data-ttu-id="758b4-122">指定此 Cmdlet 移除之網路介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="758b4-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="758b4-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="758b4-123">-PassThru</span></span>
<span data-ttu-id="758b4-124">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="758b4-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="758b4-125">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="758b4-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="758b4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="758b4-126">-ResourceGroupName</span></span>
<span data-ttu-id="758b4-127">指定包含此 Cmdlet 移除之網路介面之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="758b4-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="758b4-128">-確認</span><span class="sxs-lookup"><span data-stu-id="758b4-128">-Confirm</span></span>
<span data-ttu-id="758b4-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="758b4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="758b4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="758b4-130">-WhatIf</span></span>
<span data-ttu-id="758b4-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="758b4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="758b4-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="758b4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="758b4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="758b4-133">CommonParameters</span></span>
<span data-ttu-id="758b4-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="758b4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="758b4-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="758b4-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="758b4-136">輸入</span><span class="sxs-lookup"><span data-stu-id="758b4-136">INPUTS</span></span>

### <span data-ttu-id="758b4-137">所有</span><span class="sxs-lookup"><span data-stu-id="758b4-137">None</span></span>
<span data-ttu-id="758b4-138">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="758b4-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="758b4-139">輸出</span><span class="sxs-lookup"><span data-stu-id="758b4-139">OUTPUTS</span></span>

## <span data-ttu-id="758b4-140">筆記</span><span class="sxs-lookup"><span data-stu-id="758b4-140">NOTES</span></span>

## <span data-ttu-id="758b4-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="758b4-141">RELATED LINKS</span></span>

[<span data-ttu-id="758b4-142">AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="758b4-142">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="758b4-143">新-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="758b4-143">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="758b4-144">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="758b4-144">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)


