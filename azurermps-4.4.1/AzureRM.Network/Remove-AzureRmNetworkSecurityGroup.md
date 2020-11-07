---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: fd6d9a09bd2c4fa597d2c384d3ba8e730b3f1102
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624009"
---
# <span data-ttu-id="171e9-101">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="171e9-101">Remove-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="171e9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="171e9-102">SYNOPSIS</span></span>
<span data-ttu-id="171e9-103">移除網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="171e9-103">Removes a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="171e9-104">句法</span><span class="sxs-lookup"><span data-stu-id="171e9-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="171e9-105">說明</span><span class="sxs-lookup"><span data-stu-id="171e9-105">DESCRIPTION</span></span>
<span data-ttu-id="171e9-106">**AzureRmNetworkSecurityGroup** Cmdlet 會移除 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="171e9-106">The **Remove-AzureRmNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="171e9-107">示例</span><span class="sxs-lookup"><span data-stu-id="171e9-107">EXAMPLES</span></span>

### <span data-ttu-id="171e9-108">範例1：移除網路安全性群組</span><span class="sxs-lookup"><span data-stu-id="171e9-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzureRmNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="171e9-109">這個命令會在名為 TestRG 的資源群組中，移除名為 NSG-FrontEnd 的安全性群組。</span><span class="sxs-lookup"><span data-stu-id="171e9-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="171e9-110">參數</span><span class="sxs-lookup"><span data-stu-id="171e9-110">PARAMETERS</span></span>

### <span data-ttu-id="171e9-111">-Force</span><span class="sxs-lookup"><span data-stu-id="171e9-111">-Force</span></span>
<span data-ttu-id="171e9-112">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="171e9-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="171e9-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="171e9-113">-Name</span></span>
<span data-ttu-id="171e9-114">指定此 Cmdlet 移除之網路安全性群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="171e9-114">Specifies the name of the network security group that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="171e9-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="171e9-115">-PassThru</span></span>
<span data-ttu-id="171e9-116">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="171e9-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="171e9-117">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="171e9-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="171e9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="171e9-118">-ResourceGroupName</span></span>
<span data-ttu-id="171e9-119">指定此 Cmdlet 移除網路安全群組的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="171e9-119">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="171e9-120">-確認</span><span class="sxs-lookup"><span data-stu-id="171e9-120">-Confirm</span></span>
<span data-ttu-id="171e9-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="171e9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="171e9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="171e9-122">-WhatIf</span></span>
<span data-ttu-id="171e9-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="171e9-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="171e9-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="171e9-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="171e9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="171e9-125">-DefaultProfile</span></span>
<span data-ttu-id="171e9-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="171e9-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="171e9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="171e9-127">CommonParameters</span></span>
<span data-ttu-id="171e9-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="171e9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="171e9-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="171e9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="171e9-130">輸入</span><span class="sxs-lookup"><span data-stu-id="171e9-130">INPUTS</span></span>

## <span data-ttu-id="171e9-131">輸出</span><span class="sxs-lookup"><span data-stu-id="171e9-131">OUTPUTS</span></span>

## <span data-ttu-id="171e9-132">筆記</span><span class="sxs-lookup"><span data-stu-id="171e9-132">NOTES</span></span>

## <span data-ttu-id="171e9-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="171e9-133">RELATED LINKS</span></span>

[<span data-ttu-id="171e9-134">AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="171e9-134">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="171e9-135">新-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="171e9-135">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="171e9-136">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="171e9-136">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)


