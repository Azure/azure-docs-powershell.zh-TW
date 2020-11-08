---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
ms.openlocfilehash: 8bc586ea9543c7545e7d24e3bc6d7bc36bb77d49
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128680"
---
# <span data-ttu-id="58a3b-101">Get-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="58a3b-101">Get-AzIotHubCertificate</span></span>

## <span data-ttu-id="58a3b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="58a3b-102">SYNOPSIS</span></span>
<span data-ttu-id="58a3b-103">列出 Azure IoT 中樞中包含的所有憑證或特定憑證。</span><span class="sxs-lookup"><span data-stu-id="58a3b-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub.</span></span> 

## <span data-ttu-id="58a3b-104">句法</span><span class="sxs-lookup"><span data-stu-id="58a3b-104">SYNTAX</span></span>

### <span data-ttu-id="58a3b-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="58a3b-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58a3b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="58a3b-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificate [-InputObject] <PSIotHub> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58a3b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="58a3b-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58a3b-108">說明</span><span class="sxs-lookup"><span data-stu-id="58a3b-108">DESCRIPTION</span></span>
<span data-ttu-id="58a3b-109">如需 Azure IoT 中樞中 CA 憑證的詳細說明，請參閱 https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="58a3b-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="58a3b-110">示例</span><span class="sxs-lookup"><span data-stu-id="58a3b-110">EXAMPLES</span></span>

### <span data-ttu-id="58a3b-111">範例1</span><span class="sxs-lookup"><span data-stu-id="58a3b-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub"

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiothub3   mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiothub    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="58a3b-112">列出 MyIotHub 中的所有憑證</span><span class="sxs-lookup"><span data-stu-id="58a3b-112">List all certificates in MyIotHub</span></span>

### <span data-ttu-id="58a3b-113">範例2</span><span class="sxs-lookup"><span data-stu-id="58a3b-113">Example 2</span></span>
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

<span data-ttu-id="58a3b-114">顯示 MyCertificate 的詳細資料</span><span class="sxs-lookup"><span data-stu-id="58a3b-114">Show details about MyCertificate</span></span>

## <span data-ttu-id="58a3b-115">參數</span><span class="sxs-lookup"><span data-stu-id="58a3b-115">PARAMETERS</span></span>

### <span data-ttu-id="58a3b-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="58a3b-116">-CertificateName</span></span>
<span data-ttu-id="58a3b-117">憑證的名稱</span><span class="sxs-lookup"><span data-stu-id="58a3b-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="58a3b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58a3b-118">-DefaultProfile</span></span>
<span data-ttu-id="58a3b-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="58a3b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58a3b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58a3b-120">-InputObject</span></span>
<span data-ttu-id="58a3b-121">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="58a3b-121">IotHub Object</span></span>

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

### <span data-ttu-id="58a3b-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="58a3b-122">-Name</span></span>
<span data-ttu-id="58a3b-123">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="58a3b-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="58a3b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58a3b-124">-ResourceGroupName</span></span>
<span data-ttu-id="58a3b-125">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="58a3b-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="58a3b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58a3b-126">-ResourceId</span></span>
<span data-ttu-id="58a3b-127">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="58a3b-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="58a3b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58a3b-128">CommonParameters</span></span>
<span data-ttu-id="58a3b-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="58a3b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58a3b-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="58a3b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58a3b-131">輸入</span><span class="sxs-lookup"><span data-stu-id="58a3b-131">INPUTS</span></span>

### <span data-ttu-id="58a3b-132">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="58a3b-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="58a3b-133">System.object</span><span class="sxs-lookup"><span data-stu-id="58a3b-133">System.String</span></span>

## <span data-ttu-id="58a3b-134">輸出</span><span class="sxs-lookup"><span data-stu-id="58a3b-134">OUTPUTS</span></span>

### <span data-ttu-id="58a3b-135">PSCertificateDescription （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="58a3b-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="58a3b-136">筆記</span><span class="sxs-lookup"><span data-stu-id="58a3b-136">NOTES</span></span>

## <span data-ttu-id="58a3b-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="58a3b-137">RELATED LINKS</span></span>
