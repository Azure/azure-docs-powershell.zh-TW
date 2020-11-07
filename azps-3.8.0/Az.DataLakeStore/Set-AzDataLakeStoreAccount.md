---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreAccount.md
ms.openlocfilehash: 4db6ceb0f806aeffd4dc69580da891de567e4e83
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966482"
---
# <span data-ttu-id="b3861-101">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b3861-101">Set-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="b3861-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b3861-102">SYNOPSIS</span></span>
<span data-ttu-id="b3861-103">修改 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="b3861-103">Modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="b3861-104">句法</span><span class="sxs-lookup"><span data-stu-id="b3861-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tag] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3861-105">說明</span><span class="sxs-lookup"><span data-stu-id="b3861-105">DESCRIPTION</span></span>
<span data-ttu-id="b3861-106">**AzDataLakeStoreAccount** Cmdlet 會修改 Data Lake store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="b3861-106">The **Set-AzDataLakeStoreAccount** cmdlet modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="b3861-107">示例</span><span class="sxs-lookup"><span data-stu-id="b3861-107">EXAMPLES</span></span>

### <span data-ttu-id="b3861-108">範例1：新增標籤至帳戶</span><span class="sxs-lookup"><span data-stu-id="b3861-108">Example 1: Add a tag to an account</span></span>
```
PS C:\>Set-AzDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
```

<span data-ttu-id="b3861-109">這個命令會將指定的標記新增到名為 ContosoADL 的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="b3861-109">This command adds the specified tag to the Data Lake Store account named ContosoADL.</span></span>

## <span data-ttu-id="b3861-110">參數</span><span class="sxs-lookup"><span data-stu-id="b3861-110">PARAMETERS</span></span>

### <span data-ttu-id="b3861-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="b3861-111">-AllowAzureIpState</span></span>
<span data-ttu-id="b3861-112">選擇性地透過防火牆允許/封鎖 Azure 原始 Ip。</span><span class="sxs-lookup"><span data-stu-id="b3861-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3861-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="b3861-113">-DefaultGroup</span></span>
<span data-ttu-id="b3861-114">指定 AzureActive 目錄群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b3861-114">Specifies the ID of an AzureActive Directory group.</span></span>
<span data-ttu-id="b3861-115">這個群組是您建立的檔案和資料夾的預設群組。</span><span class="sxs-lookup"><span data-stu-id="b3861-115">This group is the default group for files and folders that you create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3861-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3861-116">-DefaultProfile</span></span>
<span data-ttu-id="b3861-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b3861-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3861-118">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="b3861-118">-FirewallState</span></span>
<span data-ttu-id="b3861-119">或者，您可以選擇啟用或停用現有的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="b3861-119">Optionally enable or disable existing firewall rules.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3861-120">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="b3861-120">-KeyVersion</span></span>
<span data-ttu-id="b3861-121">如果加密類型是 [由使用者指派]，則使用者可以使用此參數來旋轉其金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="b3861-121">If the encryption type is User assigned, the user can rotate their key version with this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3861-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="b3861-122">-Name</span></span>
<span data-ttu-id="b3861-123">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3861-123">Specifies the name of a Data Lake Store account.</span></span>

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

### <span data-ttu-id="b3861-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3861-124">-ResourceGroupName</span></span>
<span data-ttu-id="b3861-125">指定包含要修改之 Data Lake Store 帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3861-125">Specifies the name of the resource group that contains the Data Lake Store account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3861-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="b3861-126">-Tag</span></span>
<span data-ttu-id="b3861-127">將標記指定為鍵值對。</span><span class="sxs-lookup"><span data-stu-id="b3861-127">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="b3861-128">您可以使用標籤來識別來自其他 Azure 資源的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="b3861-128">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3861-129">層級</span><span class="sxs-lookup"><span data-stu-id="b3861-129">-Tier</span></span>
<span data-ttu-id="b3861-130">此帳戶要使用的預期承諾層級。</span><span class="sxs-lookup"><span data-stu-id="b3861-130">The desired commitment tier for this account to use.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TierType]
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment1TB, Commitment10TB, Commitment100TB, Commitment500TB, Commitment1PB, Commitment5PB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3861-131">-TrustedIdProviderState</span><span class="sxs-lookup"><span data-stu-id="b3861-131">-TrustedIdProviderState</span></span>
<span data-ttu-id="b3861-132">或者，您可以選擇啟用或停用現有的信任識別碼提供者。</span><span class="sxs-lookup"><span data-stu-id="b3861-132">Optionally enable or disable the existing trusted ID providers.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3861-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3861-133">CommonParameters</span></span>
<span data-ttu-id="b3861-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b3861-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3861-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b3861-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3861-136">輸入</span><span class="sxs-lookup"><span data-stu-id="b3861-136">INPUTS</span></span>

### <span data-ttu-id="b3861-137">System.object</span><span class="sxs-lookup"><span data-stu-id="b3861-137">System.String</span></span>

### <span data-ttu-id="b3861-138">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b3861-138">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b3861-139">DataLake 為 Nullable "1 [DataLake. TrustedIdProviderState，，版本 = 2.0.0.0，Culture = 中性，PublicKeyToken = 31bf3856ad364e35]]）。））））</span><span class="sxs-lookup"><span data-stu-id="b3861-139">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="b3861-140">DataLake 為 Nullable "1 [DataLake. FirewallState，，版本 = 2.0.0.0，Culture = 中性，PublicKeyToken = 31bf3856ad364e35]]）。））））</span><span class="sxs-lookup"><span data-stu-id="b3861-140">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="b3861-141">DataLake 為 Nullable "1 [DataLake. TierType，，版本 = 2.0.0.0，Culture = 中性，PublicKeyToken = 31bf3856ad364e35]]）。））））</span><span class="sxs-lookup"><span data-stu-id="b3861-141">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="b3861-142">DataLake 為 Nullable "1 [DataLake. FirewallAllowAzureIpsState，，版本 = 2.0.0.0，Culture = 中性，PublicKeyToken = 31bf3856ad364e35]]）。））））</span><span class="sxs-lookup"><span data-stu-id="b3861-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="b3861-143">輸出</span><span class="sxs-lookup"><span data-stu-id="b3861-143">OUTPUTS</span></span>

### <span data-ttu-id="b3861-144">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b3861-144">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="b3861-145">筆記</span><span class="sxs-lookup"><span data-stu-id="b3861-145">NOTES</span></span>

## <span data-ttu-id="b3861-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3861-146">RELATED LINKS</span></span>

[<span data-ttu-id="b3861-147">AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b3861-147">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="b3861-148">新-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b3861-148">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="b3861-149">移除-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b3861-149">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="b3861-150">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b3861-150">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


