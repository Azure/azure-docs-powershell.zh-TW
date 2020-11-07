---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
ms.openlocfilehash: c50ee56a5dcb15c3b199e9aaf08aeca74828cc66
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957370"
---
# <span data-ttu-id="f4003-101">Remove-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="f4003-101">Remove-AzIotHubKey</span></span>

## <span data-ttu-id="f4003-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f4003-102">SYNOPSIS</span></span>
<span data-ttu-id="f4003-103">移除 IotHub 鍵。</span><span class="sxs-lookup"><span data-stu-id="f4003-103">Removes an IotHub Key.</span></span>

## <span data-ttu-id="f4003-104">句法</span><span class="sxs-lookup"><span data-stu-id="f4003-104">SYNTAX</span></span>

### <span data-ttu-id="f4003-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f4003-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4003-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f4003-106">ResourceIdSet</span></span>
```
Remove-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4003-107">說明</span><span class="sxs-lookup"><span data-stu-id="f4003-107">DESCRIPTION</span></span>
<span data-ttu-id="f4003-108">移除 IotHub 鍵。</span><span class="sxs-lookup"><span data-stu-id="f4003-108">Removes an IotHub Key.</span></span>
<span data-ttu-id="f4003-109">如果有多個同名的按鍵，清單中的第一個按鍵就會移除。</span><span class="sxs-lookup"><span data-stu-id="f4003-109">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="f4003-110">示例</span><span class="sxs-lookup"><span data-stu-id="f4003-110">EXAMPLES</span></span>

### <span data-ttu-id="f4003-111">範例1刪除 IotHub</span><span class="sxs-lookup"><span data-stu-id="f4003-111">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="f4003-112">從名為 "myiothub" 的 IotHub 中移除名為 iothubowner1 的索引鍵</span><span class="sxs-lookup"><span data-stu-id="f4003-112">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="f4003-113">參數</span><span class="sxs-lookup"><span data-stu-id="f4003-113">PARAMETERS</span></span>

### <span data-ttu-id="f4003-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4003-114">-DefaultProfile</span></span>
<span data-ttu-id="f4003-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f4003-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4003-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="f4003-116">-HubId</span></span>
<span data-ttu-id="f4003-117">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="f4003-117">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4003-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="f4003-118">-KeyName</span></span>
<span data-ttu-id="f4003-119">索引鍵的名稱</span><span class="sxs-lookup"><span data-stu-id="f4003-119">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4003-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="f4003-120">-Name</span></span>
<span data-ttu-id="f4003-121">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="f4003-121">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4003-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4003-122">-ResourceGroupName</span></span>
<span data-ttu-id="f4003-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="f4003-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4003-124">-確認</span><span class="sxs-lookup"><span data-stu-id="f4003-124">-Confirm</span></span>
<span data-ttu-id="f4003-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f4003-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4003-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4003-126">-WhatIf</span></span>
<span data-ttu-id="f4003-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f4003-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4003-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f4003-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4003-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4003-129">CommonParameters</span></span>
<span data-ttu-id="f4003-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f4003-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4003-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f4003-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4003-132">輸入</span><span class="sxs-lookup"><span data-stu-id="f4003-132">INPUTS</span></span>

### <span data-ttu-id="f4003-133">System.object</span><span class="sxs-lookup"><span data-stu-id="f4003-133">System.String</span></span>

## <span data-ttu-id="f4003-134">輸出</span><span class="sxs-lookup"><span data-stu-id="f4003-134">OUTPUTS</span></span>

### <span data-ttu-id="f4003-135">PSSharedAccessSignatureAuthorizationRule （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="f4003-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="f4003-136">筆記</span><span class="sxs-lookup"><span data-stu-id="f4003-136">NOTES</span></span>

## <span data-ttu-id="f4003-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4003-137">RELATED LINKS</span></span>
