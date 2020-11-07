---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
ms.openlocfilehash: f73cfd1cadff449289bfa82ab1de04d110fb0f1a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787578"
---
# <span data-ttu-id="ad3ad-101">Add-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="ad3ad-101">Add-AzIotHubKey</span></span>

## <span data-ttu-id="ad3ad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ad3ad-102">SYNOPSIS</span></span>
<span data-ttu-id="ad3ad-103">建立 IotHub 鍵。</span><span class="sxs-lookup"><span data-stu-id="ad3ad-103">Creates an IotHub Key.</span></span>

## <span data-ttu-id="ad3ad-104">句法</span><span class="sxs-lookup"><span data-stu-id="ad3ad-104">SYNTAX</span></span>

```
Add-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad3ad-105">說明</span><span class="sxs-lookup"><span data-stu-id="ad3ad-105">DESCRIPTION</span></span>
<span data-ttu-id="ad3ad-106">為提供的 IotHub 建立索引鍵。</span><span class="sxs-lookup"><span data-stu-id="ad3ad-106">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="ad3ad-107">KeyNames 不是唯一的，需要謹慎管理。</span><span class="sxs-lookup"><span data-stu-id="ad3ad-107">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="ad3ad-108">示例</span><span class="sxs-lookup"><span data-stu-id="ad3ad-108">EXAMPLES</span></span>

### <span data-ttu-id="ad3ad-109">範例1新增索引鍵至 IotHub</span><span class="sxs-lookup"><span data-stu-id="ad3ad-109">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="ad3ad-110">針對具有 RegistryRead 許可權的 iothub "myiothub" 建立名為 "mykey" 的金鑰。</span><span class="sxs-lookup"><span data-stu-id="ad3ad-110">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="ad3ad-111">參數</span><span class="sxs-lookup"><span data-stu-id="ad3ad-111">PARAMETERS</span></span>

### <span data-ttu-id="ad3ad-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad3ad-112">-DefaultProfile</span></span>
<span data-ttu-id="ad3ad-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ad3ad-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad3ad-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="ad3ad-114">-KeyName</span></span>
<span data-ttu-id="ad3ad-115">索引鍵的名稱</span><span class="sxs-lookup"><span data-stu-id="ad3ad-115">Name of the Key</span></span>

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

### <span data-ttu-id="ad3ad-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="ad3ad-116">-Name</span></span>
<span data-ttu-id="ad3ad-117">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="ad3ad-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="ad3ad-118">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="ad3ad-118">-PrimaryKey</span></span>
<span data-ttu-id="ad3ad-119">主鍵</span><span class="sxs-lookup"><span data-stu-id="ad3ad-119">The primary key</span></span>

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

### <span data-ttu-id="ad3ad-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad3ad-120">-ResourceGroupName</span></span>
<span data-ttu-id="ad3ad-121">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="ad3ad-121">Resource Group Name</span></span>

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

### <span data-ttu-id="ad3ad-122">-許可權</span><span class="sxs-lookup"><span data-stu-id="ad3ad-122">-Rights</span></span>
<span data-ttu-id="ad3ad-123">此 IOTHub 的許可權</span><span class="sxs-lookup"><span data-stu-id="ad3ad-123">The permissions for this IOTHub</span></span>

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

### <span data-ttu-id="ad3ad-124">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="ad3ad-124">-SecondaryKey</span></span>
<span data-ttu-id="ad3ad-125">次要金鑰</span><span class="sxs-lookup"><span data-stu-id="ad3ad-125">The Secondary Key</span></span>

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

### <span data-ttu-id="ad3ad-126">-確認</span><span class="sxs-lookup"><span data-stu-id="ad3ad-126">-Confirm</span></span>
<span data-ttu-id="ad3ad-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ad3ad-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad3ad-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad3ad-128">-WhatIf</span></span>
<span data-ttu-id="ad3ad-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ad3ad-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad3ad-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad3ad-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad3ad-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad3ad-131">CommonParameters</span></span>
<span data-ttu-id="ad3ad-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ad3ad-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad3ad-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ad3ad-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad3ad-134">輸入</span><span class="sxs-lookup"><span data-stu-id="ad3ad-134">INPUTS</span></span>

### <span data-ttu-id="ad3ad-135">System.object</span><span class="sxs-lookup"><span data-stu-id="ad3ad-135">System.String</span></span>

## <span data-ttu-id="ad3ad-136">輸出</span><span class="sxs-lookup"><span data-stu-id="ad3ad-136">OUTPUTS</span></span>

### <span data-ttu-id="ad3ad-137">PSSharedAccessSignatureAuthorizationRule （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="ad3ad-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="ad3ad-138">筆記</span><span class="sxs-lookup"><span data-stu-id="ad3ad-138">NOTES</span></span>

## <span data-ttu-id="ad3ad-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad3ad-139">RELATED LINKS</span></span>
