---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/add-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
ms.openlocfilehash: 8141b85c3322918fc955deaa6db9abb1bbf78f8e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901665"
---
# <span data-ttu-id="03796-101">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="03796-101">Add-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="03796-102">簡介</span><span class="sxs-lookup"><span data-stu-id="03796-102">SYNOPSIS</span></span>
<span data-ttu-id="03796-103">將常用名稱或指紋新增到該組組，以用於用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="03796-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="03796-104">語法</span><span class="sxs-lookup"><span data-stu-id="03796-104">SYNTAX</span></span>

### <span data-ttu-id="03796-105">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="03796-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03796-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="03796-106">SingleUpdateWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03796-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="03796-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03796-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="03796-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03796-109">描述</span><span class="sxs-lookup"><span data-stu-id="03796-109">DESCRIPTION</span></span>
<span data-ttu-id="03796-110">使用 **Add-AzServiceFabricClientCertificate** 將通用名稱及發行者指紋或憑證指紋新增到該組，以便用戶端使用它進行驗證。</span><span class="sxs-lookup"><span data-stu-id="03796-110">Use **Add-AzServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="03796-111">例子</span><span class="sxs-lookup"><span data-stu-id="03796-111">EXAMPLES</span></span>

### <span data-ttu-id="03796-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="03796-112">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="03796-113">此命令會使用指紋 '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A'新增憑證至該組，因此用戶端可以使用憑證做為系統管理員，與組塊通訊。</span><span class="sxs-lookup"><span data-stu-id="03796-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="03796-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="03796-114">Example 2</span></span>
```
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="03796-115">此命令會新增一個唯讀的用戶端憑證，其共同名稱為 'Contoso.com'，而發行者指紋是 '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A'。</span><span class="sxs-lookup"><span data-stu-id="03796-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="03796-116">參數</span><span class="sxs-lookup"><span data-stu-id="03796-116">PARAMETERS</span></span>

### <span data-ttu-id="03796-117">-系統管理員</span><span class="sxs-lookup"><span data-stu-id="03796-117">-Admin</span></span>
<span data-ttu-id="03796-118">用戶端驗證類型</span><span class="sxs-lookup"><span data-stu-id="03796-118">Client authentication type</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SingleUpdateWithThumbprint, SingleUpdateWithCommonName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03796-119">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="03796-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="03796-120">指定只有系統管理員許可權的用戶端憑證指紋</span><span class="sxs-lookup"><span data-stu-id="03796-120">Specify client certificate thumbprint which only has admin permission</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03796-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="03796-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="03796-122">指定用戶端常用名稱、發行者指紋和驗證類型</span><span class="sxs-lookup"><span data-stu-id="03796-122">Specify client common name , issuer thumbprint and authentication type</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]
Parameter Sets: MultipleUpdatesWithCommonName
Aliases: CertCommonName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03796-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="03796-123">-CommonName</span></span>
<span data-ttu-id="03796-124">指定用戶端憑證通用名稱</span><span class="sxs-lookup"><span data-stu-id="03796-124">Specify client certificate common name</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03796-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03796-125">-DefaultProfile</span></span>
<span data-ttu-id="03796-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="03796-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03796-127">-發行者Thumbprint</span><span class="sxs-lookup"><span data-stu-id="03796-127">-IssuerThumbprint</span></span>
<span data-ttu-id="03796-128">指定用戶端憑證發行者指紋</span><span class="sxs-lookup"><span data-stu-id="03796-128">Specify thumbprint of client certificate's issuer</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03796-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="03796-129">-Name</span></span>
<span data-ttu-id="03796-130">指定組名</span><span class="sxs-lookup"><span data-stu-id="03796-130">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03796-131">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="03796-131">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="03796-132">指定只有唯讀許可權的用戶端憑證指紋</span><span class="sxs-lookup"><span data-stu-id="03796-132">Specify client certificate thumbprint which only has read only permission</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03796-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03796-133">-ResourceGroupName</span></span>
<span data-ttu-id="03796-134">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="03796-134">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="03796-135">-拇指列印</span><span class="sxs-lookup"><span data-stu-id="03796-135">-Thumbprint</span></span>
<span data-ttu-id="03796-136">指定用戶端憑證指紋</span><span class="sxs-lookup"><span data-stu-id="03796-136">Specify client certificate thumbprint</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithThumbprint
Aliases: ClientCertificateThumbprint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03796-137">-確認</span><span class="sxs-lookup"><span data-stu-id="03796-137">-Confirm</span></span>
<span data-ttu-id="03796-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="03796-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03796-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03796-139">-WhatIf</span></span>
<span data-ttu-id="03796-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="03796-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03796-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="03796-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03796-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03796-142">CommonParameters</span></span>
<span data-ttu-id="03796-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="03796-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03796-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03796-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03796-145">輸入</span><span class="sxs-lookup"><span data-stu-id="03796-145">INPUTS</span></span>

### <span data-ttu-id="03796-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="03796-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="03796-147">System.String</span><span class="sxs-lookup"><span data-stu-id="03796-147">System.String</span></span>

### <span data-ttu-id="03796-148">System.String[]</span><span class="sxs-lookup"><span data-stu-id="03796-148">System.String[]</span></span>

### <span data-ttu-id="03796-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span><span class="sxs-lookup"><span data-stu-id="03796-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="03796-150">輸出</span><span class="sxs-lookup"><span data-stu-id="03796-150">OUTPUTS</span></span>

### <span data-ttu-id="03796-151">Microsoft.Azure.Commands.ServiceFabric.models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="03796-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="03796-152">筆記</span><span class="sxs-lookup"><span data-stu-id="03796-152">NOTES</span></span>

## <span data-ttu-id="03796-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="03796-153">RELATED LINKS</span></span>

[<span data-ttu-id="03796-154">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="03796-154">Remove-AzServiceFabricClientCertificate</span></span>](./Remove-AzServiceFabricClientCertificate.md)
