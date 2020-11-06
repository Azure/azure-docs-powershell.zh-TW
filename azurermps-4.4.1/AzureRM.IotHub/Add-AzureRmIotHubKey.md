---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
ms.openlocfilehash: f7bbe0c37d03a6db372c6c70da021160060a542a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453487"
---
# <span data-ttu-id="0e92f-101">Add-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="0e92f-101">Add-AzureRmIotHubKey</span></span>

## <span data-ttu-id="0e92f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0e92f-102">SYNOPSIS</span></span>
<span data-ttu-id="0e92f-103">建立 IotHub 鍵。</span><span class="sxs-lookup"><span data-stu-id="0e92f-103">Creates an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e92f-104">句法</span><span class="sxs-lookup"><span data-stu-id="0e92f-104">SYNTAX</span></span>

```
Add-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [[-PrimaryKey] <String>] [[-SecondaryKey] <String>] [-Rights] <PSAccessRights>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e92f-105">說明</span><span class="sxs-lookup"><span data-stu-id="0e92f-105">DESCRIPTION</span></span>
<span data-ttu-id="0e92f-106">為提供的 IotHub 建立索引鍵。</span><span class="sxs-lookup"><span data-stu-id="0e92f-106">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="0e92f-107">KeyNames 不是唯一的，需要謹慎管理。</span><span class="sxs-lookup"><span data-stu-id="0e92f-107">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="0e92f-108">示例</span><span class="sxs-lookup"><span data-stu-id="0e92f-108">EXAMPLES</span></span>

### <span data-ttu-id="0e92f-109">範例1新增索引鍵至 IotHub</span><span class="sxs-lookup"><span data-stu-id="0e92f-109">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="0e92f-110">針對具有 RegistryRead 許可權的 iothub "myiothub" 建立名為 "mykey" 的金鑰。</span><span class="sxs-lookup"><span data-stu-id="0e92f-110">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="0e92f-111">參數</span><span class="sxs-lookup"><span data-stu-id="0e92f-111">PARAMETERS</span></span>

### <span data-ttu-id="0e92f-112">-KeyName</span><span class="sxs-lookup"><span data-stu-id="0e92f-112">-KeyName</span></span>
<span data-ttu-id="0e92f-113">索引鍵的名稱</span><span class="sxs-lookup"><span data-stu-id="0e92f-113">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e92f-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="0e92f-114">-Name</span></span>
<span data-ttu-id="0e92f-115">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="0e92f-115">Name of the IotHub</span></span>

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

### <span data-ttu-id="0e92f-116">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="0e92f-116">-PrimaryKey</span></span>
<span data-ttu-id="0e92f-117">主鍵</span><span class="sxs-lookup"><span data-stu-id="0e92f-117">The primary key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e92f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e92f-118">-ResourceGroupName</span></span>
<span data-ttu-id="0e92f-119">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="0e92f-119">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e92f-120">-許可權</span><span class="sxs-lookup"><span data-stu-id="0e92f-120">-Rights</span></span>
<span data-ttu-id="0e92f-121">此 IOTHub 的許可權</span><span class="sxs-lookup"><span data-stu-id="0e92f-121">The permissions for this IOTHub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights
Parameter Sets: (All)
Aliases: 
Accepted values: RegistryRead, RegistryWrite, ServiceConnect, DeviceConnect

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e92f-122">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="0e92f-122">-SecondaryKey</span></span>
<span data-ttu-id="0e92f-123">次要金鑰</span><span class="sxs-lookup"><span data-stu-id="0e92f-123">The Secondary Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e92f-124">-確認</span><span class="sxs-lookup"><span data-stu-id="0e92f-124">-Confirm</span></span>
<span data-ttu-id="0e92f-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0e92f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e92f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e92f-126">-WhatIf</span></span>
<span data-ttu-id="0e92f-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0e92f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e92f-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0e92f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e92f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e92f-129">-DefaultProfile</span></span>
<span data-ttu-id="0e92f-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0e92f-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e92f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e92f-131">CommonParameters</span></span>
<span data-ttu-id="0e92f-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0e92f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e92f-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0e92f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e92f-134">輸入</span><span class="sxs-lookup"><span data-stu-id="0e92f-134">INPUTS</span></span>

### <span data-ttu-id="0e92f-135">System.object</span><span class="sxs-lookup"><span data-stu-id="0e92f-135">System.String</span></span>
<span data-ttu-id="0e92f-136">PSAccessRights （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="0e92f-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights</span></span>

## <span data-ttu-id="0e92f-137">輸出</span><span class="sxs-lookup"><span data-stu-id="0e92f-137">OUTPUTS</span></span>

### <span data-ttu-id="0e92f-138">PSSharedAccessSignatureAuthorizationRule （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="0e92f-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="0e92f-139">\` \[ \[ PSSharedAccessSignatureAuthorizationRule、IotHub = 1.0.0.0、Culture = 中性、PublicKeyToken = null、Culture = 中立、版本 = 1.0.0.0、Culture = 中性、PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="0e92f-139">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="0e92f-140">筆記</span><span class="sxs-lookup"><span data-stu-id="0e92f-140">NOTES</span></span>

## <span data-ttu-id="0e92f-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="0e92f-141">RELATED LINKS</span></span>

