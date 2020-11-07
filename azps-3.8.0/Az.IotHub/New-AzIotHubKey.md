---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
ms.openlocfilehash: cc843ca942ae79fe76e1dd50e76c876e4d05b5ac
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959747"
---
# <span data-ttu-id="b9ee6-101">New-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="b9ee6-101">New-AzIotHubKey</span></span>

## <span data-ttu-id="b9ee6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b9ee6-102">SYNOPSIS</span></span>
<span data-ttu-id="b9ee6-103">產生 Azure IoT 中樞金鑰。</span><span class="sxs-lookup"><span data-stu-id="b9ee6-103">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="b9ee6-104">句法</span><span class="sxs-lookup"><span data-stu-id="b9ee6-104">SYNTAX</span></span>

### <span data-ttu-id="b9ee6-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b9ee6-105">ResourceSet (Default)</span></span>
```
New-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9ee6-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b9ee6-106">ResourceIdSet</span></span>
```
New-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9ee6-107">說明</span><span class="sxs-lookup"><span data-stu-id="b9ee6-107">DESCRIPTION</span></span>
<span data-ttu-id="b9ee6-108">產生 Azure IoT 中樞金鑰。</span><span class="sxs-lookup"><span data-stu-id="b9ee6-108">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="b9ee6-109">示例</span><span class="sxs-lookup"><span data-stu-id="b9ee6-109">EXAMPLES</span></span>

### <span data-ttu-id="b9ee6-110">範例1重新產生主鍵</span><span class="sxs-lookup"><span data-stu-id="b9ee6-110">Example 1 Regenerate primary key</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "primary"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=    6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=        ServiceConnect
```

<span data-ttu-id="b9ee6-111">針對 azure iot 中樞的授權原則 "testKey" 重新產生主金鑰。</span><span class="sxs-lookup"><span data-stu-id="b9ee6-111">Regenerated primary key for the authorization policy "testKey" of an azure iot hub.</span></span>

### <span data-ttu-id="b9ee6-112">範例2交換按鍵</span><span class="sxs-lookup"><span data-stu-id="b9ee6-112">Example 2 Swapping keys</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "swap"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=    SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=        ServiceConnect
```

<span data-ttu-id="b9ee6-113">交換 azure iot 中樞之授權原則 "testKey" 的按鍵。</span><span class="sxs-lookup"><span data-stu-id="b9ee6-113">Swapping keys for the authorization policy "testKey" of an azure iot hub.</span></span>

## <span data-ttu-id="b9ee6-114">參數</span><span class="sxs-lookup"><span data-stu-id="b9ee6-114">PARAMETERS</span></span>

### <span data-ttu-id="b9ee6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9ee6-115">-DefaultProfile</span></span>
<span data-ttu-id="b9ee6-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b9ee6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9ee6-117">-HubId</span><span class="sxs-lookup"><span data-stu-id="b9ee6-117">-HubId</span></span>
<span data-ttu-id="b9ee6-118">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b9ee6-118">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b9ee6-119">-KeyName</span><span class="sxs-lookup"><span data-stu-id="b9ee6-119">-KeyName</span></span>
<span data-ttu-id="b9ee6-120">索引鍵的名稱</span><span class="sxs-lookup"><span data-stu-id="b9ee6-120">Name of the Key</span></span>

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

### <span data-ttu-id="b9ee6-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="b9ee6-121">-Name</span></span>
<span data-ttu-id="b9ee6-122">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="b9ee6-122">Name of the IotHub</span></span>

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

### <span data-ttu-id="b9ee6-123">-RenewKey</span><span class="sxs-lookup"><span data-stu-id="b9ee6-123">-RenewKey</span></span>
<span data-ttu-id="b9ee6-124">重新產生金鑰。</span><span class="sxs-lookup"><span data-stu-id="b9ee6-124">Regenerate Key.</span></span>

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

### <span data-ttu-id="b9ee6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9ee6-125">-ResourceGroupName</span></span>
<span data-ttu-id="b9ee6-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="b9ee6-126">Resource Group Name</span></span>

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

### <span data-ttu-id="b9ee6-127">-確認</span><span class="sxs-lookup"><span data-stu-id="b9ee6-127">-Confirm</span></span>
<span data-ttu-id="b9ee6-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b9ee6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9ee6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9ee6-129">-WhatIf</span></span>
<span data-ttu-id="b9ee6-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b9ee6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9ee6-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b9ee6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9ee6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9ee6-132">CommonParameters</span></span>
<span data-ttu-id="b9ee6-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b9ee6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9ee6-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b9ee6-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9ee6-135">輸入</span><span class="sxs-lookup"><span data-stu-id="b9ee6-135">INPUTS</span></span>

### <span data-ttu-id="b9ee6-136">System.object</span><span class="sxs-lookup"><span data-stu-id="b9ee6-136">System.String</span></span>

## <span data-ttu-id="b9ee6-137">輸出</span><span class="sxs-lookup"><span data-stu-id="b9ee6-137">OUTPUTS</span></span>

### <span data-ttu-id="b9ee6-138">PSSharedAccessSignatureAuthorizationRule （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="b9ee6-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="b9ee6-139">筆記</span><span class="sxs-lookup"><span data-stu-id="b9ee6-139">NOTES</span></span>

## <span data-ttu-id="b9ee6-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="b9ee6-140">RELATED LINKS</span></span>
