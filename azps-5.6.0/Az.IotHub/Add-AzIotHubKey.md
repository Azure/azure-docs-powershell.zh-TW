---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
ms.openlocfilehash: fe964ba2672c67fc9bb5e47e7b7a16d4fdd49471
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913866"
---
# <span data-ttu-id="cd18b-101">Add-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="cd18b-101">Add-AzIotHubKey</span></span>

## <span data-ttu-id="cd18b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cd18b-102">SYNOPSIS</span></span>
<span data-ttu-id="cd18b-103">建立 IotHub 金鑰。</span><span class="sxs-lookup"><span data-stu-id="cd18b-103">Creates an IotHub Key.</span></span>

## <span data-ttu-id="cd18b-104">語法</span><span class="sxs-lookup"><span data-stu-id="cd18b-104">SYNTAX</span></span>

### <span data-ttu-id="cd18b-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="cd18b-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd18b-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cd18b-106">ResourceIdSet</span></span>
```
Add-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd18b-107">描述</span><span class="sxs-lookup"><span data-stu-id="cd18b-107">DESCRIPTION</span></span>
<span data-ttu-id="cd18b-108">為提供的 IotHub 建立金鑰。</span><span class="sxs-lookup"><span data-stu-id="cd18b-108">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="cd18b-109">KeyName 並非唯一，必須小心管理。</span><span class="sxs-lookup"><span data-stu-id="cd18b-109">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="cd18b-110">例子</span><span class="sxs-lookup"><span data-stu-id="cd18b-110">EXAMPLES</span></span>

### <span data-ttu-id="cd18b-111">範例 1 新增金鑰至 IotHub</span><span class="sxs-lookup"><span data-stu-id="cd18b-111">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="cd18b-112">為具有 RegistryRead 許可權的 iothub "myiothub" 建立名為 "mykey" 的金鑰。</span><span class="sxs-lookup"><span data-stu-id="cd18b-112">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="cd18b-113">參數</span><span class="sxs-lookup"><span data-stu-id="cd18b-113">PARAMETERS</span></span>

### <span data-ttu-id="cd18b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd18b-114">-DefaultProfile</span></span>
<span data-ttu-id="cd18b-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="cd18b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd18b-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="cd18b-116">-HubId</span></span>
<span data-ttu-id="cd18b-117">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="cd18b-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="cd18b-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="cd18b-118">-KeyName</span></span>
<span data-ttu-id="cd18b-119">金鑰名稱</span><span class="sxs-lookup"><span data-stu-id="cd18b-119">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd18b-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="cd18b-120">-Name</span></span>
<span data-ttu-id="cd18b-121">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="cd18b-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="cd18b-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="cd18b-122">-PrimaryKey</span></span>
<span data-ttu-id="cd18b-123">主鍵</span><span class="sxs-lookup"><span data-stu-id="cd18b-123">The primary key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd18b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd18b-124">-ResourceGroupName</span></span>
<span data-ttu-id="cd18b-125">資源組名</span><span class="sxs-lookup"><span data-stu-id="cd18b-125">Resource Group Name</span></span>

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

### <span data-ttu-id="cd18b-126">-Rights</span><span class="sxs-lookup"><span data-stu-id="cd18b-126">-Rights</span></span>
<span data-ttu-id="cd18b-127">此 IOTHub 的許可權</span><span class="sxs-lookup"><span data-stu-id="cd18b-127">The permissions for this IOTHub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights
Parameter Sets: (All)
Aliases:
Accepted values: RegistryRead, RegistryWrite, ServiceConnect, DeviceConnect

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd18b-128">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="cd18b-128">-SecondaryKey</span></span>
<span data-ttu-id="cd18b-129">次要鍵</span><span class="sxs-lookup"><span data-stu-id="cd18b-129">The Secondary Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd18b-130">-確認</span><span class="sxs-lookup"><span data-stu-id="cd18b-130">-Confirm</span></span>
<span data-ttu-id="cd18b-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cd18b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd18b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd18b-132">-WhatIf</span></span>
<span data-ttu-id="cd18b-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cd18b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd18b-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd18b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd18b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd18b-135">CommonParameters</span></span>
<span data-ttu-id="cd18b-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cd18b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd18b-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="cd18b-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd18b-138">輸入</span><span class="sxs-lookup"><span data-stu-id="cd18b-138">INPUTS</span></span>

### <span data-ttu-id="cd18b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="cd18b-139">System.String</span></span>

## <span data-ttu-id="cd18b-140">輸出</span><span class="sxs-lookup"><span data-stu-id="cd18b-140">OUTPUTS</span></span>

### <span data-ttu-id="cd18b-141">Microsoft.Azure.Commands.management.IotHub.models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cd18b-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="cd18b-142">筆記</span><span class="sxs-lookup"><span data-stu-id="cd18b-142">NOTES</span></span>

## <span data-ttu-id="cd18b-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="cd18b-143">RELATED LINKS</span></span>
