---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationsecuritygroup
schema: 2.0.0
ms.openlocfilehash: 48121e165eea27b57ec36301a657a6778f4c14b7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800385"
---
# <span data-ttu-id="cb8d8-101">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cb8d8-101">Remove-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="cb8d8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb8d8-102">SYNOPSIS</span></span>
<span data-ttu-id="cb8d8-103">移除應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="cb8d8-103">Removes an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb8d8-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb8d8-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb8d8-105">說明</span><span class="sxs-lookup"><span data-stu-id="cb8d8-105">DESCRIPTION</span></span>
<span data-ttu-id="cb8d8-106">**AzureRmApplicationSecurityGroup** Cmdlet 會移除應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="cb8d8-106">The **Remove-AzureRmApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="cb8d8-107">示例</span><span class="sxs-lookup"><span data-stu-id="cb8d8-107">EXAMPLES</span></span>

### <span data-ttu-id="cb8d8-108">範例1</span><span class="sxs-lookup"><span data-stu-id="cb8d8-108">Example 1</span></span>
```
PS C:\>Remove-AzureRmApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="cb8d8-109">這個命令會刪除名為 MyResourceGroup 的資源群組中名為 MyApplicationSecurityGrouo 的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="cb8d8-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="cb8d8-110">參數</span><span class="sxs-lookup"><span data-stu-id="cb8d8-110">PARAMETERS</span></span>

### <span data-ttu-id="cb8d8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb8d8-111">-DefaultProfile</span></span>
<span data-ttu-id="cb8d8-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cb8d8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb8d8-113">-Force</span><span class="sxs-lookup"><span data-stu-id="cb8d8-113">-Force</span></span>
<span data-ttu-id="cb8d8-114">如果您想要刪除資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="cb8d8-114">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="cb8d8-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="cb8d8-115">-Name</span></span>
<span data-ttu-id="cb8d8-116">應用程式安全性群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb8d8-116">The name of the application security group.</span></span>

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

### <span data-ttu-id="cb8d8-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb8d8-117">-PassThru</span></span>
<span data-ttu-id="cb8d8-118">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="cb8d8-118">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="cb8d8-119">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="cb8d8-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cb8d8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb8d8-120">-ResourceGroupName</span></span>
<span data-ttu-id="cb8d8-121">應用程式安全性群組的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="cb8d8-121">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="cb8d8-122">-確認</span><span class="sxs-lookup"><span data-stu-id="cb8d8-122">-Confirm</span></span>
<span data-ttu-id="cb8d8-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cb8d8-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb8d8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb8d8-124">-WhatIf</span></span>
<span data-ttu-id="cb8d8-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cb8d8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb8d8-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb8d8-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb8d8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb8d8-127">CommonParameters</span></span>
<span data-ttu-id="cb8d8-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb8d8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb8d8-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cb8d8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb8d8-130">輸入</span><span class="sxs-lookup"><span data-stu-id="cb8d8-130">INPUTS</span></span>

### <span data-ttu-id="cb8d8-131">System.object</span><span class="sxs-lookup"><span data-stu-id="cb8d8-131">System.String</span></span>

## <span data-ttu-id="cb8d8-132">輸出</span><span class="sxs-lookup"><span data-stu-id="cb8d8-132">OUTPUTS</span></span>

### <span data-ttu-id="cb8d8-133">System.object</span><span class="sxs-lookup"><span data-stu-id="cb8d8-133">System.Object</span></span>

## <span data-ttu-id="cb8d8-134">筆記</span><span class="sxs-lookup"><span data-stu-id="cb8d8-134">NOTES</span></span>

## <span data-ttu-id="cb8d8-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb8d8-135">RELATED LINKS</span></span>

[<span data-ttu-id="cb8d8-136">新-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cb8d8-136">New-AzureRmApplicationSecurityGroup</span></span>](./New-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="cb8d8-137">AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cb8d8-137">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)
