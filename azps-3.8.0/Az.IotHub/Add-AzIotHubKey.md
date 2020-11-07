---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
ms.openlocfilehash: 422eb25456beb57ed6ab029fa5d70a47061ca491
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956407"
---
# <span data-ttu-id="673cd-101">Add-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="673cd-101">Add-AzIotHubKey</span></span>

## <span data-ttu-id="673cd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="673cd-102">SYNOPSIS</span></span>
<span data-ttu-id="673cd-103">建立 IotHub 鍵。</span><span class="sxs-lookup"><span data-stu-id="673cd-103">Creates an IotHub Key.</span></span>

## <span data-ttu-id="673cd-104">句法</span><span class="sxs-lookup"><span data-stu-id="673cd-104">SYNTAX</span></span>

### <span data-ttu-id="673cd-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="673cd-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="673cd-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="673cd-106">ResourceIdSet</span></span>
```
Add-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="673cd-107">說明</span><span class="sxs-lookup"><span data-stu-id="673cd-107">DESCRIPTION</span></span>
<span data-ttu-id="673cd-108">為提供的 IotHub 建立索引鍵。</span><span class="sxs-lookup"><span data-stu-id="673cd-108">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="673cd-109">KeyNames 不是唯一的，需要謹慎管理。</span><span class="sxs-lookup"><span data-stu-id="673cd-109">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="673cd-110">示例</span><span class="sxs-lookup"><span data-stu-id="673cd-110">EXAMPLES</span></span>

### <span data-ttu-id="673cd-111">範例1新增索引鍵至 IotHub</span><span class="sxs-lookup"><span data-stu-id="673cd-111">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="673cd-112">針對具有 RegistryRead 許可權的 iothub "myiothub" 建立名為 "mykey" 的金鑰。</span><span class="sxs-lookup"><span data-stu-id="673cd-112">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="673cd-113">參數</span><span class="sxs-lookup"><span data-stu-id="673cd-113">PARAMETERS</span></span>

### <span data-ttu-id="673cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="673cd-114">-DefaultProfile</span></span>
<span data-ttu-id="673cd-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="673cd-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="673cd-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="673cd-116">-HubId</span></span>
<span data-ttu-id="673cd-117">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="673cd-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="673cd-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="673cd-118">-KeyName</span></span>
<span data-ttu-id="673cd-119">索引鍵的名稱</span><span class="sxs-lookup"><span data-stu-id="673cd-119">Name of the Key</span></span>

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

### <span data-ttu-id="673cd-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="673cd-120">-Name</span></span>
<span data-ttu-id="673cd-121">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="673cd-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="673cd-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="673cd-122">-PrimaryKey</span></span>
<span data-ttu-id="673cd-123">主鍵</span><span class="sxs-lookup"><span data-stu-id="673cd-123">The primary key</span></span>

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

### <span data-ttu-id="673cd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="673cd-124">-ResourceGroupName</span></span>
<span data-ttu-id="673cd-125">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="673cd-125">Resource Group Name</span></span>

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

### <span data-ttu-id="673cd-126">-許可權</span><span class="sxs-lookup"><span data-stu-id="673cd-126">-Rights</span></span>
<span data-ttu-id="673cd-127">此 IOTHub 的許可權</span><span class="sxs-lookup"><span data-stu-id="673cd-127">The permissions for this IOTHub</span></span>

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

### <span data-ttu-id="673cd-128">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="673cd-128">-SecondaryKey</span></span>
<span data-ttu-id="673cd-129">次要金鑰</span><span class="sxs-lookup"><span data-stu-id="673cd-129">The Secondary Key</span></span>

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

### <span data-ttu-id="673cd-130">-確認</span><span class="sxs-lookup"><span data-stu-id="673cd-130">-Confirm</span></span>
<span data-ttu-id="673cd-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="673cd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="673cd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="673cd-132">-WhatIf</span></span>
<span data-ttu-id="673cd-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="673cd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="673cd-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="673cd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="673cd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="673cd-135">CommonParameters</span></span>
<span data-ttu-id="673cd-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="673cd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="673cd-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="673cd-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="673cd-138">輸入</span><span class="sxs-lookup"><span data-stu-id="673cd-138">INPUTS</span></span>

### <span data-ttu-id="673cd-139">System.object</span><span class="sxs-lookup"><span data-stu-id="673cd-139">System.String</span></span>

## <span data-ttu-id="673cd-140">輸出</span><span class="sxs-lookup"><span data-stu-id="673cd-140">OUTPUTS</span></span>

### <span data-ttu-id="673cd-141">PSSharedAccessSignatureAuthorizationRule （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="673cd-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="673cd-142">筆記</span><span class="sxs-lookup"><span data-stu-id="673cd-142">NOTES</span></span>

## <span data-ttu-id="673cd-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="673cd-143">RELATED LINKS</span></span>
