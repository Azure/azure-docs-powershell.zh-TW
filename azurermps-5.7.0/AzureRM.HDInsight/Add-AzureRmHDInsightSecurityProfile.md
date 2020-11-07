---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightsecurityprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightSecurityProfile.md
ms.openlocfilehash: 41571439400810214bee7f0f3f646e6444998982
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623975"
---
# <span data-ttu-id="ad7c1-101">Add-AzureRmHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="ad7c1-101">Add-AzureRmHDInsightSecurityProfile</span></span>

## <span data-ttu-id="ad7c1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ad7c1-102">SYNOPSIS</span></span>
<span data-ttu-id="ad7c1-103">在群集設定物件中新增安全性 profileto。</span><span class="sxs-lookup"><span data-stu-id="ad7c1-103">Adds a security profileto a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad7c1-104">句法</span><span class="sxs-lookup"><span data-stu-id="ad7c1-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -Domain <String>
 -DomainUserCredential <PSCredential> -OrganizationalUnitDN <String> -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ad7c1-105">說明</span><span class="sxs-lookup"><span data-stu-id="ad7c1-105">DESCRIPTION</span></span>
<span data-ttu-id="ad7c1-106">安全設定檔是透過 kerberizing 來建立安全的群集。</span><span class="sxs-lookup"><span data-stu-id="ad7c1-106">Security profile is used to create a secure cluster by kerberizing it.</span></span>
<span data-ttu-id="ad7c1-107">安全性設定檔包含將群集加入 Active Directory 網域的相關設定。</span><span class="sxs-lookup"><span data-stu-id="ad7c1-107">Security profile contains configuration related joining the cluster to Active Directory Domain.</span></span>

## <span data-ttu-id="ad7c1-108">示例</span><span class="sxs-lookup"><span data-stu-id="ad7c1-108">EXAMPLES</span></span>

### <span data-ttu-id="ad7c1-109">範例1</span><span class="sxs-lookup"><span data-stu-id="ad7c1-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="ad7c1-110">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="ad7c1-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="ad7c1-111">參數</span><span class="sxs-lookup"><span data-stu-id="ad7c1-111">PARAMETERS</span></span>

### <span data-ttu-id="ad7c1-112">-ClusterUsersGroupDNs</span><span class="sxs-lookup"><span data-stu-id="ad7c1-112">-ClusterUsersGroupDNs</span></span>
<span data-ttu-id="ad7c1-113">將可在 Ambari 和 Ranger 中使用之 Active Directory 群組的可分辨名稱</span><span class="sxs-lookup"><span data-stu-id="ad7c1-113">Distinguished names of the Active Directory groups that will be available in Ambari and Ranger</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad7c1-114">-Config</span><span class="sxs-lookup"><span data-stu-id="ad7c1-114">-Config</span></span>
<span data-ttu-id="ad7c1-115">指定此 Cmdlet 修改的 HDInsight 群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="ad7c1-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="ad7c1-116">這個物件是由 New-AzureRmHDInsightClusterConfig Cmdlet 建立的。</span><span class="sxs-lookup"><span data-stu-id="ad7c1-116">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad7c1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad7c1-117">-DefaultProfile</span></span>
<span data-ttu-id="ad7c1-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ad7c1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad7c1-119">-網域</span><span class="sxs-lookup"><span data-stu-id="ad7c1-119">-Domain</span></span>
<span data-ttu-id="ad7c1-120">群集的 Active Directory 網域</span><span class="sxs-lookup"><span data-stu-id="ad7c1-120">Active Directory domain for the cluster</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad7c1-121">-DomainUserCredential</span><span class="sxs-lookup"><span data-stu-id="ad7c1-121">-DomainUserCredential</span></span>
<span data-ttu-id="ad7c1-122">具有足夠許可權的網域使用者帳號憑證來建立群集。</span><span class="sxs-lookup"><span data-stu-id="ad7c1-122">A domain user account credential with sufficient permissions for creating the cluster.</span></span>
<span data-ttu-id="ad7c1-123">[使用者名] 應為 [ user@domain 格式]</span><span class="sxs-lookup"><span data-stu-id="ad7c1-123">Username should be in user@domain format</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad7c1-124">-LdapsUrls</span><span class="sxs-lookup"><span data-stu-id="ad7c1-124">-LdapsUrls</span></span>
<span data-ttu-id="ad7c1-125">Active Directory 的一或多個 LDAPS 伺服器的 url</span><span class="sxs-lookup"><span data-stu-id="ad7c1-125">Urls of one or multiple LDAPS servers for the Active Directory</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad7c1-126">-OrganizationalUnitDN</span><span class="sxs-lookup"><span data-stu-id="ad7c1-126">-OrganizationalUnitDN</span></span>
<span data-ttu-id="ad7c1-127">在 Active directory 中將會建立使用者和電腦帳戶的組織單位的可分辨名稱</span><span class="sxs-lookup"><span data-stu-id="ad7c1-127">Distinguished name of the organizational unit in the Active directory where user and computer accounts will be created</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad7c1-128">-確認</span><span class="sxs-lookup"><span data-stu-id="ad7c1-128">-Confirm</span></span>
<span data-ttu-id="ad7c1-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ad7c1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad7c1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad7c1-130">-WhatIf</span></span>
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

### <span data-ttu-id="ad7c1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad7c1-131">CommonParameters</span></span>
<span data-ttu-id="ad7c1-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ad7c1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad7c1-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ad7c1-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad7c1-134">輸入</span><span class="sxs-lookup"><span data-stu-id="ad7c1-134">INPUTS</span></span>

### <span data-ttu-id="ad7c1-135">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="ad7c1-135">AzureHDInsightConfig</span></span>
<span data-ttu-id="ad7c1-136">形參 "Config" 接受管線中 "AzureHDInsightConfig" 類型的值</span><span class="sxs-lookup"><span data-stu-id="ad7c1-136">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="ad7c1-137">輸出</span><span class="sxs-lookup"><span data-stu-id="ad7c1-137">OUTPUTS</span></span>

### <span data-ttu-id="ad7c1-138">AzureHDInsightSecurityProfile （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="ad7c1-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span></span>

## <span data-ttu-id="ad7c1-139">筆記</span><span class="sxs-lookup"><span data-stu-id="ad7c1-139">NOTES</span></span>

## <span data-ttu-id="ad7c1-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad7c1-140">RELATED LINKS</span></span>

