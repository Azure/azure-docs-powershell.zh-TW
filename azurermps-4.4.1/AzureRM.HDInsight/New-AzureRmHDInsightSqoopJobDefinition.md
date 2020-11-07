---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 769406d0eb47672fcaaea8acfb3b3fdccd6810d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626007"
---
# <span data-ttu-id="f917e-101">New-AzureRmHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f917e-101">New-AzureRmHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="f917e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f917e-102">SYNOPSIS</span></span>
<span data-ttu-id="f917e-103">建立 Sqoop 工作物件。</span><span class="sxs-lookup"><span data-stu-id="f917e-103">Creates a Sqoop job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f917e-104">句法</span><span class="sxs-lookup"><span data-stu-id="f917e-104">SYNTAX</span></span>

```
New-AzureRmHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f917e-105">說明</span><span class="sxs-lookup"><span data-stu-id="f917e-105">DESCRIPTION</span></span>
<span data-ttu-id="f917e-106">**新的-AzureRmHDInsightSqoopJobDefinition** Cmdlet 定義用於 Azure HDInsight 群集的 Sqoop 工作物件。</span><span class="sxs-lookup"><span data-stu-id="f917e-106">The **New-AzureRmHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="f917e-107">示例</span><span class="sxs-lookup"><span data-stu-id="f917e-107">EXAMPLES</span></span>

### <span data-ttu-id="f917e-108">範例1：建立 Sqoop 作業定義</span><span class="sxs-lookup"><span data-stu-id="f917e-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzureRmHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="f917e-109">這個命令會建立 Sqoop 作業定義。</span><span class="sxs-lookup"><span data-stu-id="f917e-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="f917e-110">參數</span><span class="sxs-lookup"><span data-stu-id="f917e-110">PARAMETERS</span></span>

### <span data-ttu-id="f917e-111">-Command</span><span class="sxs-lookup"><span data-stu-id="f917e-111">-Command</span></span>
<span data-ttu-id="f917e-112">指定 [Sqoop] 命令。</span><span class="sxs-lookup"><span data-stu-id="f917e-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="f917e-113">檔案</span><span class="sxs-lookup"><span data-stu-id="f917e-113">-File</span></span>
<span data-ttu-id="f917e-114">指定包含要執行之查詢之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="f917e-114">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="f917e-115">該檔案必須在與群集相關聯的儲存空間帳戶上提供。</span><span class="sxs-lookup"><span data-stu-id="f917e-115">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="f917e-116">您可以使用這個參數，而不是 *Query* 參數。</span><span class="sxs-lookup"><span data-stu-id="f917e-116">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="f917e-117">-檔案</span><span class="sxs-lookup"><span data-stu-id="f917e-117">-Files</span></span>
<span data-ttu-id="f917e-118">指定與 Hive 作業相關聯的檔案集合。</span><span class="sxs-lookup"><span data-stu-id="f917e-118">Specifies a collection of files that are associated with a Hive job.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f917e-119">-LibDir</span><span class="sxs-lookup"><span data-stu-id="f917e-119">-LibDir</span></span>
<span data-ttu-id="f917e-120">指定 Sqoop 作業的文件庫目錄。</span><span class="sxs-lookup"><span data-stu-id="f917e-120">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="f917e-121">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="f917e-121">-StatusFolder</span></span>
<span data-ttu-id="f917e-122">指定包含工作之標準輸出和錯誤輸出的資料夾位置。</span><span class="sxs-lookup"><span data-stu-id="f917e-122">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="f917e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f917e-123">-DefaultProfile</span></span>
<span data-ttu-id="f917e-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f917e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f917e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f917e-125">CommonParameters</span></span>
<span data-ttu-id="f917e-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f917e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f917e-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f917e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f917e-128">輸入</span><span class="sxs-lookup"><span data-stu-id="f917e-128">INPUTS</span></span>

## <span data-ttu-id="f917e-129">輸出</span><span class="sxs-lookup"><span data-stu-id="f917e-129">OUTPUTS</span></span>

### <span data-ttu-id="f917e-130">AzureHDInsightSqoopJobDefinition （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="f917e-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="f917e-131">筆記</span><span class="sxs-lookup"><span data-stu-id="f917e-131">NOTES</span></span>

## <span data-ttu-id="f917e-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="f917e-132">RELATED LINKS</span></span>

[<span data-ttu-id="f917e-133">開始-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f917e-133">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


