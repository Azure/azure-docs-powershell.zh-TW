---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
ms.openlocfilehash: 56613276907772cfe3f2cbd99810ff247485913f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790374"
---
# <span data-ttu-id="6f4bb-101">Get-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="6f4bb-101">Get-AzNetAppFilesPool</span></span>

## <span data-ttu-id="6f4bb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6f4bb-102">SYNOPSIS</span></span>
<span data-ttu-id="6f4bb-103">取得 (ANF) 池的 Azure NetApp 檔案的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6f4bb-103">Gets details of an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="6f4bb-104">句法</span><span class="sxs-lookup"><span data-stu-id="6f4bb-104">SYNTAX</span></span>

### <span data-ttu-id="6f4bb-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6f4bb-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f4bb-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f4bb-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f4bb-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f4bb-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesPool -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6f4bb-108">說明</span><span class="sxs-lookup"><span data-stu-id="6f4bb-108">DESCRIPTION</span></span>
<span data-ttu-id="6f4bb-109">**AzNetAppFilesPool** Cmdlet 會取得 ANF 池的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6f4bb-109">The **Get-AzNetAppFilesPool** cmdlet gets details of an ANF pool.</span></span>

## <span data-ttu-id="6f4bb-110">示例</span><span class="sxs-lookup"><span data-stu-id="6f4bb-110">EXAMPLES</span></span>

### <span data-ttu-id="6f4bb-111">範例1：取得 ANF 池</span><span class="sxs-lookup"><span data-stu-id="6f4bb-111">Example 1: Get an ANF pool</span></span>
```
PS C:\>Get-AzAnfPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyAnfPool"

Output:

Location          : westus2
Id                : /subscriptions/subsID/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : a3a53a09-fd70-37ab-39dc-392a04cba525
Size              : 4398046511104
ServiceLevel      : Premium
ProvisioningState : Succeeded
```

<span data-ttu-id="6f4bb-112">這個命令會從帳戶 "MyAnfAccount" 中取得名為 MyAnfPool 的帳戶。</span><span class="sxs-lookup"><span data-stu-id="6f4bb-112">This command gets the account named MyAnfPool from the account "MyAnfAccount".</span></span>

## <span data-ttu-id="6f4bb-113">參數</span><span class="sxs-lookup"><span data-stu-id="6f4bb-113">PARAMETERS</span></span>

### <span data-ttu-id="6f4bb-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6f4bb-114">-AccountName</span></span>
<span data-ttu-id="6f4bb-115">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="6f4bb-115">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f4bb-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="6f4bb-116">-AccountObject</span></span>
<span data-ttu-id="6f4bb-117">包含要傳回之池的帳戶物件</span><span class="sxs-lookup"><span data-stu-id="6f4bb-117">The account object containing the pool to return</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f4bb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f4bb-118">-DefaultProfile</span></span>
<span data-ttu-id="6f4bb-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6f4bb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f4bb-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="6f4bb-120">-Name</span></span>
<span data-ttu-id="6f4bb-121">ANF 池的名稱</span><span class="sxs-lookup"><span data-stu-id="6f4bb-121">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: PoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f4bb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f4bb-122">-ResourceGroupName</span></span>
<span data-ttu-id="6f4bb-123">ANF 池的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="6f4bb-123">The resource group of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f4bb-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f4bb-124">-ResourceId</span></span>
<span data-ttu-id="6f4bb-125">ANF 池的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="6f4bb-125">The resource id of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f4bb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f4bb-126">CommonParameters</span></span>
<span data-ttu-id="6f4bb-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6f4bb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6f4bb-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6f4bb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f4bb-129">輸入</span><span class="sxs-lookup"><span data-stu-id="6f4bb-129">INPUTS</span></span>

### <span data-ttu-id="6f4bb-130">System.object</span><span class="sxs-lookup"><span data-stu-id="6f4bb-130">System.String</span></span>

### <span data-ttu-id="6f4bb-131">PSNetAppFilesAccount 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="6f4bb-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="6f4bb-132">輸出</span><span class="sxs-lookup"><span data-stu-id="6f4bb-132">OUTPUTS</span></span>

### <span data-ttu-id="6f4bb-133">PSNetAppFilesPool 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="6f4bb-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="6f4bb-134">筆記</span><span class="sxs-lookup"><span data-stu-id="6f4bb-134">NOTES</span></span>

## <span data-ttu-id="6f4bb-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f4bb-135">RELATED LINKS</span></span>
