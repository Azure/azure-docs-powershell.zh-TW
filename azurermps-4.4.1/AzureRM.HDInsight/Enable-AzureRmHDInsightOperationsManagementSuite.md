---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Enable-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Enable-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: fcaa5c1342801c4c0ef00e1a4c48abf4a6b4da41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624564"
---
# <span data-ttu-id="d89d1-101">Enable-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="d89d1-101">Enable-AzureRmHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="d89d1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d89d1-102">SYNOPSIS</span></span>
<span data-ttu-id="d89d1-103">在 HDInsight 群集中啟用操作管理套件 (OMS) ，而相關的記錄將會傳送到 enable 中指定的 OMS 工作區。</span><span class="sxs-lookup"><span data-stu-id="d89d1-103">Enables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will be sent to the OMS workspace specified during enable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d89d1-104">句法</span><span class="sxs-lookup"><span data-stu-id="d89d1-104">SYNTAX</span></span>

```
Enable-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-WorkspaceId] <String>
 [-PrimaryKey] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d89d1-105">說明</span><span class="sxs-lookup"><span data-stu-id="d89d1-105">DESCRIPTION</span></span>
<span data-ttu-id="d89d1-106">**Enable-AzureRmHDInsightOperationsManagementSuite** Cmdlet 可在 Azure HDInsight 群集中 (OMS) 的操作管理套件。</span><span class="sxs-lookup"><span data-stu-id="d89d1-106">The **Enable-AzureRmHDInsightOperationsManagementSuite** cmdlet enables Operations Management Suite (OMS) in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="d89d1-107">示例</span><span class="sxs-lookup"><span data-stu-id="d89d1-107">EXAMPLES</span></span>

### <span data-ttu-id="d89d1-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d89d1-108">Example 1</span></span>
```
PS C:\> Enable-AzureRmHDInsightOMS -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="d89d1-109">將會在 HDInsight 群集上啟用 Operations Management Suite (OMS) ，並將相關的記錄傳送到具有識別碼1d364e89-bb71-4503-aa3d-a23535aea7bd 的 OMS 工作區。</span><span class="sxs-lookup"><span data-stu-id="d89d1-109">Operations Management Suite (OMS) will be enabled on the HDInsight cluster and relevant logs will be sent to the OMS workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="d89d1-110">範例2</span><span class="sxs-lookup"><span data-stu-id="d89d1-110">Example 2</span></span>
```
PS C:\> Enable-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="d89d1-111">將會在 HDInsight 群集上啟用 Operations Management Suite (OMS) ，並將相關的記錄傳送到具有識別碼1d364e89-bb71-4503-aa3d-a23535aea7bd 的 OMS 工作區。</span><span class="sxs-lookup"><span data-stu-id="d89d1-111">Operations Management Suite (OMS) will be enabled on the HDInsight cluster and relevant logs will be sent to the OMS workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="d89d1-112">參數</span><span class="sxs-lookup"><span data-stu-id="d89d1-112">PARAMETERS</span></span>

### <span data-ttu-id="d89d1-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="d89d1-113">-Name</span></span>
<span data-ttu-id="d89d1-114">要啟用運營管理套件 (OMS) 的群集名稱。</span><span class="sxs-lookup"><span data-stu-id="d89d1-114">The name of the cluster to enable Operations Management Suite(OMS).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d89d1-115">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="d89d1-115">-PrimaryKey</span></span>
<span data-ttu-id="d89d1-116">運營管理套件的主鍵 (OMS) 工作區。</span><span class="sxs-lookup"><span data-stu-id="d89d1-116">The primary key of the Operations Management Suite(OMS) workspace.</span></span>

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

### <span data-ttu-id="d89d1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d89d1-117">-ResourceGroupName</span></span>
<span data-ttu-id="d89d1-118">群集的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="d89d1-118">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="d89d1-119">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="d89d1-119">-WorkspaceId</span></span>
<span data-ttu-id="d89d1-120">作業管理套件 (OMS) 工作區的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d89d1-120">The id of the Operations Management Suite(OMS) workspace.</span></span>

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

### <span data-ttu-id="d89d1-121">-確認</span><span class="sxs-lookup"><span data-stu-id="d89d1-121">-Confirm</span></span>
<span data-ttu-id="d89d1-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d89d1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d89d1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d89d1-123">-DefaultProfile</span></span>
<span data-ttu-id="d89d1-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d89d1-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d89d1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d89d1-125">-WhatIf</span></span>
<span data-ttu-id="d89d1-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d89d1-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d89d1-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d89d1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d89d1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d89d1-128">CommonParameters</span></span>
<span data-ttu-id="d89d1-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d89d1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d89d1-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d89d1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d89d1-131">輸入</span><span class="sxs-lookup"><span data-stu-id="d89d1-131">INPUTS</span></span>

### <span data-ttu-id="d89d1-132">System.object</span><span class="sxs-lookup"><span data-stu-id="d89d1-132">System.String</span></span>

## <span data-ttu-id="d89d1-133">輸出</span><span class="sxs-lookup"><span data-stu-id="d89d1-133">OUTPUTS</span></span>

### <span data-ttu-id="d89d1-134">OperationResource 中的 [Azure.]</span><span class="sxs-lookup"><span data-stu-id="d89d1-134">Microsoft.Azure.Management.HDInsight.Models.OperationResource</span></span>

## <span data-ttu-id="d89d1-135">筆記</span><span class="sxs-lookup"><span data-stu-id="d89d1-135">NOTES</span></span>

## <span data-ttu-id="d89d1-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="d89d1-136">RELATED LINKS</span></span>
