---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/new-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
ms.openlocfilehash: 7dd27544e3304570cf3fbdae861b21eabd300c35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906166"
---
# <span data-ttu-id="0ade8-101">New-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="0ade8-101">New-AzIotHubKey</span></span>

## <span data-ttu-id="0ade8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0ade8-102">SYNOPSIS</span></span>
<span data-ttu-id="0ade8-103">產生 Azure IoT Hub 金鑰。</span><span class="sxs-lookup"><span data-stu-id="0ade8-103">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="0ade8-104">語法</span><span class="sxs-lookup"><span data-stu-id="0ade8-104">SYNTAX</span></span>

### <span data-ttu-id="0ade8-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0ade8-105">ResourceSet (Default)</span></span>
```
New-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ade8-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0ade8-106">ResourceIdSet</span></span>
```
New-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ade8-107">描述</span><span class="sxs-lookup"><span data-stu-id="0ade8-107">DESCRIPTION</span></span>
<span data-ttu-id="0ade8-108">產生 Azure IoT Hub 金鑰。</span><span class="sxs-lookup"><span data-stu-id="0ade8-108">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="0ade8-109">例子</span><span class="sxs-lookup"><span data-stu-id="0ade8-109">EXAMPLES</span></span>

### <span data-ttu-id="0ade8-110">範例 1 重新產生主鍵</span><span class="sxs-lookup"><span data-stu-id="0ade8-110">Example 1 Regenerate primary key</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "primary"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=    6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=        ServiceConnect
```

<span data-ttu-id="0ade8-111">為 Azure iot 中樞的授權策略「testKey」重新產生主鍵。</span><span class="sxs-lookup"><span data-stu-id="0ade8-111">Regenerated primary key for the authorization policy "testKey" of an azure iot hub.</span></span>

### <span data-ttu-id="0ade8-112">範例 2 交換金鑰</span><span class="sxs-lookup"><span data-stu-id="0ade8-112">Example 2 Swapping keys</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "swap"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=    SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=        ServiceConnect
```

<span data-ttu-id="0ade8-113">將金鑰交換為 Azure iot 中樞的授權策略「testKey」。</span><span class="sxs-lookup"><span data-stu-id="0ade8-113">Swapping keys for the authorization policy "testKey" of an azure iot hub.</span></span>

## <span data-ttu-id="0ade8-114">參數</span><span class="sxs-lookup"><span data-stu-id="0ade8-114">PARAMETERS</span></span>

### <span data-ttu-id="0ade8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ade8-115">-DefaultProfile</span></span>
<span data-ttu-id="0ade8-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="0ade8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ade8-117">-HubId</span><span class="sxs-lookup"><span data-stu-id="0ade8-117">-HubId</span></span>
<span data-ttu-id="0ade8-118">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="0ade8-118">IotHub Resource Id</span></span>

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

### <span data-ttu-id="0ade8-119">-KeyName</span><span class="sxs-lookup"><span data-stu-id="0ade8-119">-KeyName</span></span>
<span data-ttu-id="0ade8-120">金鑰名稱</span><span class="sxs-lookup"><span data-stu-id="0ade8-120">Name of the Key</span></span>

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

### <span data-ttu-id="0ade8-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="0ade8-121">-Name</span></span>
<span data-ttu-id="0ade8-122">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="0ade8-122">Name of the IotHub</span></span>

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

### <span data-ttu-id="0ade8-123">-RenewKey</span><span class="sxs-lookup"><span data-stu-id="0ade8-123">-RenewKey</span></span>
<span data-ttu-id="0ade8-124">重新產生金鑰。</span><span class="sxs-lookup"><span data-stu-id="0ade8-124">Regenerate Key.</span></span>

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

### <span data-ttu-id="0ade8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ade8-125">-ResourceGroupName</span></span>
<span data-ttu-id="0ade8-126">資源組名</span><span class="sxs-lookup"><span data-stu-id="0ade8-126">Resource Group Name</span></span>

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

### <span data-ttu-id="0ade8-127">-確認</span><span class="sxs-lookup"><span data-stu-id="0ade8-127">-Confirm</span></span>
<span data-ttu-id="0ade8-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0ade8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ade8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ade8-129">-WhatIf</span></span>
<span data-ttu-id="0ade8-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0ade8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ade8-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0ade8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ade8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ade8-132">CommonParameters</span></span>
<span data-ttu-id="0ade8-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0ade8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ade8-134">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="0ade8-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ade8-135">輸入</span><span class="sxs-lookup"><span data-stu-id="0ade8-135">INPUTS</span></span>

### <span data-ttu-id="0ade8-136">System.String</span><span class="sxs-lookup"><span data-stu-id="0ade8-136">System.String</span></span>

## <span data-ttu-id="0ade8-137">輸出</span><span class="sxs-lookup"><span data-stu-id="0ade8-137">OUTPUTS</span></span>

### <span data-ttu-id="0ade8-138">Microsoft.Azure.Commands.management.IotHub.models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0ade8-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="0ade8-139">筆記</span><span class="sxs-lookup"><span data-stu-id="0ade8-139">NOTES</span></span>

## <span data-ttu-id="0ade8-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="0ade8-140">RELATED LINKS</span></span>
