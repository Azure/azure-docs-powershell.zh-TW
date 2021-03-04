---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
ms.openlocfilehash: 06a6f2ea8ffbd0d90689a24d3fcec5ca8222f9ca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911098"
---
# <span data-ttu-id="0a83d-101">Get-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="0a83d-101">Get-AzIotHubCertificate</span></span>

## <span data-ttu-id="0a83d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0a83d-102">SYNOPSIS</span></span>
<span data-ttu-id="0a83d-103">列出 Azure IoT 中心中包含的所有憑證或特定憑證。</span><span class="sxs-lookup"><span data-stu-id="0a83d-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub.</span></span> 

## <span data-ttu-id="0a83d-104">語法</span><span class="sxs-lookup"><span data-stu-id="0a83d-104">SYNTAX</span></span>

### <span data-ttu-id="0a83d-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0a83d-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a83d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0a83d-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificate [-InputObject] <PSIotHub> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a83d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0a83d-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a83d-108">描述</span><span class="sxs-lookup"><span data-stu-id="0a83d-108">DESCRIPTION</span></span>
<span data-ttu-id="0a83d-109">有關 Azure IoT Hub 中 CA 憑證的詳細說明，請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="0a83d-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="0a83d-110">例子</span><span class="sxs-lookup"><span data-stu-id="0a83d-110">EXAMPLES</span></span>

### <span data-ttu-id="0a83d-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="0a83d-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub"

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiothub3   mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiothub    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="0a83d-112">在 MyIotHub 中列出所有憑證</span><span class="sxs-lookup"><span data-stu-id="0a83d-112">List all certificates in MyIotHub</span></span>

### <span data-ttu-id="0a83d-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="0a83d-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="0a83d-114">顯示 MyCertificate 的詳細資訊</span><span class="sxs-lookup"><span data-stu-id="0a83d-114">Show details about MyCertificate</span></span>

## <span data-ttu-id="0a83d-115">參數</span><span class="sxs-lookup"><span data-stu-id="0a83d-115">PARAMETERS</span></span>

### <span data-ttu-id="0a83d-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="0a83d-116">-CertificateName</span></span>
<span data-ttu-id="0a83d-117">憑證名稱</span><span class="sxs-lookup"><span data-stu-id="0a83d-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="0a83d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a83d-118">-DefaultProfile</span></span>
<span data-ttu-id="0a83d-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0a83d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a83d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a83d-120">-InputObject</span></span>
<span data-ttu-id="0a83d-121">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="0a83d-121">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a83d-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="0a83d-122">-Name</span></span>
<span data-ttu-id="0a83d-123">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="0a83d-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a83d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a83d-124">-ResourceGroupName</span></span>
<span data-ttu-id="0a83d-125">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="0a83d-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0a83d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a83d-126">-ResourceId</span></span>
<span data-ttu-id="0a83d-127">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="0a83d-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="0a83d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a83d-128">CommonParameters</span></span>
<span data-ttu-id="0a83d-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0a83d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a83d-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="0a83d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a83d-131">輸入</span><span class="sxs-lookup"><span data-stu-id="0a83d-131">INPUTS</span></span>

### <span data-ttu-id="0a83d-132">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="0a83d-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="0a83d-133">System.String</span><span class="sxs-lookup"><span data-stu-id="0a83d-133">System.String</span></span>

## <span data-ttu-id="0a83d-134">輸出</span><span class="sxs-lookup"><span data-stu-id="0a83d-134">OUTPUTS</span></span>

### <span data-ttu-id="0a83d-135">Microsoft.Azure.Commands.management.IotHub.models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="0a83d-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="0a83d-136">筆記</span><span class="sxs-lookup"><span data-stu-id="0a83d-136">NOTES</span></span>

## <span data-ttu-id="0a83d-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a83d-137">RELATED LINKS</span></span>
