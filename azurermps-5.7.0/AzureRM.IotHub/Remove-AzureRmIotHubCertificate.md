---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubCertificate.md
ms.openlocfilehash: cc9bc7ef4171ea59f79f6e4687dddea4bc1dbae1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448649"
---
# <span data-ttu-id="9b984-101">Remove-AzureRmIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="9b984-101">Remove-AzureRmIotHubCertificate</span></span>

## <span data-ttu-id="9b984-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9b984-102">SYNOPSIS</span></span>
<span data-ttu-id="9b984-103">刪除 Azure IoT 中樞憑證。</span><span class="sxs-lookup"><span data-stu-id="9b984-103">Deletes an Azure IoT Hub certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b984-104">句法</span><span class="sxs-lookup"><span data-stu-id="9b984-104">SYNTAX</span></span>

### <span data-ttu-id="9b984-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9b984-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b984-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9b984-106">InputObjectSet</span></span>
```
Remove-AzureRmIotHubCertificate [-InputObject] <PSCertificateDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b984-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9b984-107">ResourceIdSet</span></span>
```
Remove-AzureRmIotHubCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b984-108">說明</span><span class="sxs-lookup"><span data-stu-id="9b984-108">DESCRIPTION</span></span>
<span data-ttu-id="9b984-109">如需 Azure IoT 中樞中 CA 憑證的詳細說明，請參閱 https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="9b984-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="9b984-110">示例</span><span class="sxs-lookup"><span data-stu-id="9b984-110">EXAMPLES</span></span>

### <span data-ttu-id="9b984-111">範例1</span><span class="sxs-lookup"><span data-stu-id="9b984-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="
```

<span data-ttu-id="9b984-112">刪除 MyCertificate</span><span class="sxs-lookup"><span data-stu-id="9b984-112">Deletes MyCertificate</span></span>

## <span data-ttu-id="9b984-113">參數</span><span class="sxs-lookup"><span data-stu-id="9b984-113">PARAMETERS</span></span>

### <span data-ttu-id="9b984-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="9b984-114">-CertificateName</span></span>
<span data-ttu-id="9b984-115">憑證的名稱</span><span class="sxs-lookup"><span data-stu-id="9b984-115">Name of the Certificate</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b984-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b984-116">-DefaultProfile</span></span>
<span data-ttu-id="9b984-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b984-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b984-118">-Etag</span><span class="sxs-lookup"><span data-stu-id="9b984-118">-Etag</span></span>
<span data-ttu-id="9b984-119">憑證的 Etag</span><span class="sxs-lookup"><span data-stu-id="9b984-119">Etag of the Certificate</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b984-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b984-120">-InputObject</span></span>
<span data-ttu-id="9b984-121">憑證物件</span><span class="sxs-lookup"><span data-stu-id="9b984-121">Certificate Object</span></span>

```yaml
Type: PSCertificateDescription
Parameter Sets: InputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b984-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="9b984-122">-Name</span></span>
<span data-ttu-id="9b984-123">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="9b984-123">Name of the Iot Hub</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b984-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b984-124">-PassThru</span></span>
<span data-ttu-id="9b984-125">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="9b984-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9b984-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b984-126">-ResourceGroupName</span></span>
<span data-ttu-id="9b984-127">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="9b984-127">Name of the Resource Group</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b984-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b984-128">-ResourceId</span></span>
<span data-ttu-id="9b984-129">憑證資源識別碼</span><span class="sxs-lookup"><span data-stu-id="9b984-129">Certificate Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b984-130">-確認</span><span class="sxs-lookup"><span data-stu-id="9b984-130">-Confirm</span></span>
<span data-ttu-id="9b984-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9b984-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b984-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b984-132">-WhatIf</span></span>
<span data-ttu-id="9b984-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9b984-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b984-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9b984-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b984-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b984-135">CommonParameters</span></span>
<span data-ttu-id="9b984-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9b984-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b984-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9b984-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b984-138">輸入</span><span class="sxs-lookup"><span data-stu-id="9b984-138">INPUTS</span></span>

### <span data-ttu-id="9b984-139">System.object</span><span class="sxs-lookup"><span data-stu-id="9b984-139">System.String</span></span>

## <span data-ttu-id="9b984-140">輸出</span><span class="sxs-lookup"><span data-stu-id="9b984-140">OUTPUTS</span></span>

### <span data-ttu-id="9b984-141">System.object</span><span class="sxs-lookup"><span data-stu-id="9b984-141">System.Boolean</span></span>

## <span data-ttu-id="9b984-142">筆記</span><span class="sxs-lookup"><span data-stu-id="9b984-142">NOTES</span></span>

## <span data-ttu-id="9b984-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b984-143">RELATED LINKS</span></span>
