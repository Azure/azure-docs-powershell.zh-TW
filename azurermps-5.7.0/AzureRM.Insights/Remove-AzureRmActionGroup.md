---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActionGroup.md
ms.openlocfilehash: 1d4a5365ac2112364a544eb2481a3193f23519c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452243"
---
# <span data-ttu-id="4131c-101">Remove-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="4131c-101">Remove-AzureRmActionGroup</span></span>

## <span data-ttu-id="4131c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4131c-102">SYNOPSIS</span></span>
<span data-ttu-id="4131c-103">移除動作群組。</span><span class="sxs-lookup"><span data-stu-id="4131c-103">Removes an action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4131c-104">句法</span><span class="sxs-lookup"><span data-stu-id="4131c-104">SYNTAX</span></span>

### <span data-ttu-id="4131c-105">ByPropertyName (預設) </span><span class="sxs-lookup"><span data-stu-id="4131c-105">ByPropertyName (Default)</span></span>
```
Remove-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4131c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4131c-106">ByResourceId</span></span>
```
Remove-AzureRmActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4131c-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4131c-107">ByInputObject</span></span>
```
Remove-AzureRmActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4131c-108">說明</span><span class="sxs-lookup"><span data-stu-id="4131c-108">DESCRIPTION</span></span>
<span data-ttu-id="4131c-109">**AzureRmActionGroup** Cmdlet 會移除 [動作] 群組。</span><span class="sxs-lookup"><span data-stu-id="4131c-109">The **Remove-AzureRmActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="4131c-110">示例</span><span class="sxs-lookup"><span data-stu-id="4131c-110">EXAMPLES</span></span>

### <span data-ttu-id="4131c-111">範例1：移除動作群組</span><span class="sxs-lookup"><span data-stu-id="4131c-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzureRmActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="4131c-112">參數</span><span class="sxs-lookup"><span data-stu-id="4131c-112">PARAMETERS</span></span>

### <span data-ttu-id="4131c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4131c-113">-DefaultProfile</span></span>
<span data-ttu-id="4131c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4131c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4131c-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4131c-115">-InputObject</span></span>
<span data-ttu-id="4131c-116">[動作] 群組 resourc</span><span class="sxs-lookup"><span data-stu-id="4131c-116">The action group resourc</span></span>

```yaml
Type: PSActionGroupResource
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4131c-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="4131c-117">-Name</span></span>
<span data-ttu-id="4131c-118">動作群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4131c-118">The name of the action group.</span></span>

```yaml
Type: String
Parameter Sets: ByPropertyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4131c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4131c-119">-ResourceGroupName</span></span>
<span data-ttu-id="4131c-120">資源群組</span><span class="sxs-lookup"><span data-stu-id="4131c-120">The resource group nam</span></span>

```yaml
Type: String
Parameter Sets: ByPropertyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4131c-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4131c-121">-ResourceId</span></span>
<span data-ttu-id="4131c-122">資源 i</span><span class="sxs-lookup"><span data-stu-id="4131c-122">The resource i</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4131c-123">-確認</span><span class="sxs-lookup"><span data-stu-id="4131c-123">-Confirm</span></span>
<span data-ttu-id="4131c-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4131c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4131c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4131c-125">-WhatIf</span></span>
<span data-ttu-id="4131c-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4131c-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4131c-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4131c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4131c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4131c-128">CommonParameters</span></span>
<span data-ttu-id="4131c-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4131c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4131c-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4131c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4131c-131">輸入</span><span class="sxs-lookup"><span data-stu-id="4131c-131">INPUTS</span></span>

### <span data-ttu-id="4131c-132">所有</span><span class="sxs-lookup"><span data-stu-id="4131c-132">None</span></span>
<span data-ttu-id="4131c-133">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="4131c-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4131c-134">輸出</span><span class="sxs-lookup"><span data-stu-id="4131c-134">OUTPUTS</span></span>

### <span data-ttu-id="4131c-135">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="4131c-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="4131c-136">筆記</span><span class="sxs-lookup"><span data-stu-id="4131c-136">NOTES</span></span>

## <span data-ttu-id="4131c-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="4131c-137">RELATED LINKS</span></span>

<span data-ttu-id="4131c-138">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
[AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
[新-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="4131c-138">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
