---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
ms.openlocfilehash: d9a6936dec16f1723c0e74db7958093aca02ce97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909794"
---
# <span data-ttu-id="56e9e-101">Remove-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="56e9e-101">Remove-AzIotHubKey</span></span>

## <span data-ttu-id="56e9e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="56e9e-102">SYNOPSIS</span></span>
<span data-ttu-id="56e9e-103">移除 IotHub 金鑰。</span><span class="sxs-lookup"><span data-stu-id="56e9e-103">Removes an IotHub Key.</span></span>

## <span data-ttu-id="56e9e-104">語法</span><span class="sxs-lookup"><span data-stu-id="56e9e-104">SYNTAX</span></span>

### <span data-ttu-id="56e9e-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="56e9e-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56e9e-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="56e9e-106">ResourceIdSet</span></span>
```
Remove-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56e9e-107">描述</span><span class="sxs-lookup"><span data-stu-id="56e9e-107">DESCRIPTION</span></span>
<span data-ttu-id="56e9e-108">移除 IotHub 金鑰。</span><span class="sxs-lookup"><span data-stu-id="56e9e-108">Removes an IotHub Key.</span></span>
<span data-ttu-id="56e9e-109">如果有多個名稱相同的按鍵，清單中第一個按鍵會移除。</span><span class="sxs-lookup"><span data-stu-id="56e9e-109">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="56e9e-110">例子</span><span class="sxs-lookup"><span data-stu-id="56e9e-110">EXAMPLES</span></span>

### <span data-ttu-id="56e9e-111">範例 1 刪除 IotHub</span><span class="sxs-lookup"><span data-stu-id="56e9e-111">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="56e9e-112">從名為"myiothub" 的 IotHub 移除名為 iothubowner1 的金鑰</span><span class="sxs-lookup"><span data-stu-id="56e9e-112">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="56e9e-113">參數</span><span class="sxs-lookup"><span data-stu-id="56e9e-113">PARAMETERS</span></span>

### <span data-ttu-id="56e9e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56e9e-114">-DefaultProfile</span></span>
<span data-ttu-id="56e9e-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="56e9e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56e9e-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="56e9e-116">-HubId</span></span>
<span data-ttu-id="56e9e-117">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="56e9e-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="56e9e-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="56e9e-118">-KeyName</span></span>
<span data-ttu-id="56e9e-119">金鑰名稱</span><span class="sxs-lookup"><span data-stu-id="56e9e-119">Name of the Key</span></span>

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

### <span data-ttu-id="56e9e-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="56e9e-120">-Name</span></span>
<span data-ttu-id="56e9e-121">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="56e9e-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="56e9e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56e9e-122">-ResourceGroupName</span></span>
<span data-ttu-id="56e9e-123">資源組名</span><span class="sxs-lookup"><span data-stu-id="56e9e-123">Resource Group Name</span></span>

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

### <span data-ttu-id="56e9e-124">-確認</span><span class="sxs-lookup"><span data-stu-id="56e9e-124">-Confirm</span></span>
<span data-ttu-id="56e9e-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="56e9e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56e9e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56e9e-126">-WhatIf</span></span>
<span data-ttu-id="56e9e-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="56e9e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56e9e-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="56e9e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56e9e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56e9e-129">CommonParameters</span></span>
<span data-ttu-id="56e9e-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="56e9e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56e9e-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="56e9e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56e9e-132">輸入</span><span class="sxs-lookup"><span data-stu-id="56e9e-132">INPUTS</span></span>

### <span data-ttu-id="56e9e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="56e9e-133">System.String</span></span>

## <span data-ttu-id="56e9e-134">輸出</span><span class="sxs-lookup"><span data-stu-id="56e9e-134">OUTPUTS</span></span>

### <span data-ttu-id="56e9e-135">Microsoft.Azure.Commands.management.IotHub.models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="56e9e-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="56e9e-136">筆記</span><span class="sxs-lookup"><span data-stu-id="56e9e-136">NOTES</span></span>

## <span data-ttu-id="56e9e-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="56e9e-137">RELATED LINKS</span></span>
