---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 99ac8e367c42cd59b3f055aa4a86a3efd4f297a0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800777"
---
# <span data-ttu-id="03042-101">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="03042-101">Remove-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="03042-102">摘要</span><span class="sxs-lookup"><span data-stu-id="03042-102">SYNOPSIS</span></span>
<span data-ttu-id="03042-103">移除應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="03042-103">Removes an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03042-104">句法</span><span class="sxs-lookup"><span data-stu-id="03042-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03042-105">說明</span><span class="sxs-lookup"><span data-stu-id="03042-105">DESCRIPTION</span></span>
<span data-ttu-id="03042-106">**AzureRmApplicationGateway** Cmdlet 會移除應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="03042-106">The **Remove-AzureRmApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="03042-107">示例</span><span class="sxs-lookup"><span data-stu-id="03042-107">EXAMPLES</span></span>

### <span data-ttu-id="03042-108">範例1：移除指定的應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="03042-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="03042-109">這個命令會移除名為 ResourceGroup01 的資源群組中名為 ApplicationGateway01 的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="03042-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="03042-110">參數</span><span class="sxs-lookup"><span data-stu-id="03042-110">PARAMETERS</span></span>

### <span data-ttu-id="03042-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03042-111">-DefaultProfile</span></span>
<span data-ttu-id="03042-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="03042-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03042-113">-Force</span><span class="sxs-lookup"><span data-stu-id="03042-113">-Force</span></span>
<span data-ttu-id="03042-114">表示無論是否指派資源，該 Cmdlet 都會強制刪除應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="03042-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03042-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="03042-115">-Name</span></span>
<span data-ttu-id="03042-116">指定要移除之應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="03042-116">Specifies the name of the application gateway to be removed.</span></span>

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

### <span data-ttu-id="03042-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03042-117">-PassThru</span></span>
<span data-ttu-id="03042-118">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="03042-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="03042-119">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="03042-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="03042-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03042-120">-ResourceGroupName</span></span>
<span data-ttu-id="03042-121">指定應用程式閘道所屬之資源組名稱的名稱。</span><span class="sxs-lookup"><span data-stu-id="03042-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="03042-122">-確認</span><span class="sxs-lookup"><span data-stu-id="03042-122">-Confirm</span></span>
<span data-ttu-id="03042-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="03042-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03042-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03042-124">-WhatIf</span></span>
<span data-ttu-id="03042-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="03042-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03042-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="03042-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03042-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03042-127">CommonParameters</span></span>
<span data-ttu-id="03042-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="03042-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03042-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="03042-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03042-130">輸入</span><span class="sxs-lookup"><span data-stu-id="03042-130">INPUTS</span></span>

## <span data-ttu-id="03042-131">輸出</span><span class="sxs-lookup"><span data-stu-id="03042-131">OUTPUTS</span></span>

### <span data-ttu-id="03042-132">System.object</span><span class="sxs-lookup"><span data-stu-id="03042-132">System.String</span></span>

## <span data-ttu-id="03042-133">筆記</span><span class="sxs-lookup"><span data-stu-id="03042-133">NOTES</span></span>

## <span data-ttu-id="03042-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="03042-134">RELATED LINKS</span></span>

[<span data-ttu-id="03042-135">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="03042-135">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)


