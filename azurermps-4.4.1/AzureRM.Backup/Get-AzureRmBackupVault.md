---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 95FF3F7A-5CC6-4AA6-A393-5EBB5579D9A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
ms.openlocfilehash: ef4d8ca2e1fb21165281375b3d325f5fc8b6ceed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447165"
---
# <span data-ttu-id="4dd64-101">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="4dd64-101">Get-AzureRmBackupVault</span></span>

## <span data-ttu-id="4dd64-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4dd64-102">SYNOPSIS</span></span>
<span data-ttu-id="4dd64-103">取得備份保存庫。</span><span class="sxs-lookup"><span data-stu-id="4dd64-103">Gets Backup vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4dd64-104">句法</span><span class="sxs-lookup"><span data-stu-id="4dd64-104">SYNTAX</span></span>

```
Get-AzureRmBackupVault [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4dd64-105">說明</span><span class="sxs-lookup"><span data-stu-id="4dd64-105">DESCRIPTION</span></span>
<span data-ttu-id="4dd64-106">**AzureRmBackupVault** Cmdlet 會取得 Azure 備份保存庫。</span><span class="sxs-lookup"><span data-stu-id="4dd64-106">The **Get-AzureRmBackupVault** cmdlet gets Azure Backup vaults.</span></span>
<span data-ttu-id="4dd64-107">這個 Cmdlet 會傳回 **AzureRmBackupVault** 物件，以與其他 Cmdlet 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="4dd64-107">This cmdlet returns **AzureRmBackupVault** objects for use with other cmdlets.</span></span>

## <span data-ttu-id="4dd64-108">示例</span><span class="sxs-lookup"><span data-stu-id="4dd64-108">EXAMPLES</span></span>

### <span data-ttu-id="4dd64-109">範例1：查看所有備份電子倉庫</span><span class="sxs-lookup"><span data-stu-id="4dd64-109">Example 1: View all the Backup vaults</span></span>
```
PS C:\>Get-AzureRmBackupVault
```

<span data-ttu-id="4dd64-110">這個命令會取得所有的 Azure 備份保存庫。</span><span class="sxs-lookup"><span data-stu-id="4dd64-110">This command gets all the Azure Backup vaults.</span></span>

### <span data-ttu-id="4dd64-111">範例2：查看在美國西部中建立的所有電子倉庫</span><span class="sxs-lookup"><span data-stu-id="4dd64-111">Example 2: View all vaults created in West US</span></span>
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Region -eq "westus" }
```

<span data-ttu-id="4dd64-112">這個命令會取得所有備份保存庫。</span><span class="sxs-lookup"><span data-stu-id="4dd64-112">This command gets all the Backup vaults.</span></span>
<span data-ttu-id="4dd64-113">透過使用管線運算子，命令會將它們傳遞到 Where-Object Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4dd64-113">The command passes them to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4dd64-114">該 Cmdlet 會根據 **Region** 屬性來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="4dd64-114">That cmdlet filters the results based on the **Region** property.</span></span>
<span data-ttu-id="4dd64-115">如需詳細資訊，請輸入 `Get-Help Where-Object` 。</span><span class="sxs-lookup"><span data-stu-id="4dd64-115">For more information, type `Get-Help Where-Object`.</span></span>

### <span data-ttu-id="4dd64-116">範例3：取得特定的電子倉庫</span><span class="sxs-lookup"><span data-stu-id="4dd64-116">Example 3: Get a specific vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup011/providers/Microsoft.Backup
                    /BackupVault/Vault
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

<span data-ttu-id="4dd64-117">這個命令會取得名為 Vault03 的保存庫。</span><span class="sxs-lookup"><span data-stu-id="4dd64-117">This command gets the vault named Vault03.</span></span>

### <span data-ttu-id="4dd64-118">範例4：計算擁有本機冗余儲存空間的電子倉庫數</span><span class="sxs-lookup"><span data-stu-id="4dd64-118">Example 4: Count the number of vaults that have locally redundant storage</span></span>
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Storage -match "LocallyRedundant" } | Measure-Object
Count    : 4
Average  : 
Sum      : 
Maximum  : 
Minimum  : 
Property :
```

<span data-ttu-id="4dd64-119">這個命令會取得所有的 Azure 備份保存庫。</span><span class="sxs-lookup"><span data-stu-id="4dd64-119">This command gets all the Azure Backup vaults.</span></span>
<span data-ttu-id="4dd64-120">該命令會將它們傳遞到物件，而 **物件** 會根據 [ **儲存空間** ] 屬性來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="4dd64-120">The command passes them to **Where-Object** , which filters the results based on the **Storage** property.</span></span>
<span data-ttu-id="4dd64-121">命令會將具有 LocallyRedundant 值的專案傳遞給 Measure-Object Cmdlet，以計算結果。</span><span class="sxs-lookup"><span data-stu-id="4dd64-121">The command passes the ones that have a value of LocallyRedundant to the Measure-Object cmdlet, which counts the results.</span></span>
<span data-ttu-id="4dd64-122">如需詳細資訊，請輸入 `Get-Help Measure-Object` 。</span><span class="sxs-lookup"><span data-stu-id="4dd64-122">For more information, type `Get-Help Measure-Object`.</span></span>

## <span data-ttu-id="4dd64-123">參數</span><span class="sxs-lookup"><span data-stu-id="4dd64-123">PARAMETERS</span></span>

### <span data-ttu-id="4dd64-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="4dd64-124">-Name</span></span>
<span data-ttu-id="4dd64-125">指定此 Cmdlet 取得的備份保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="4dd64-125">Specifies the name of the Backup vault that this cmdlet gets.</span></span>
<span data-ttu-id="4dd64-126">如果有多個備份保存庫具有相同名稱，此 Cmdlet 會將它們全部返回。</span><span class="sxs-lookup"><span data-stu-id="4dd64-126">If more than one Backup vault has the same name, this cmdlet returns them all.</span></span>
<span data-ttu-id="4dd64-127">指定 *ResourceGroupName* 參數以取得唯一的保存庫。</span><span class="sxs-lookup"><span data-stu-id="4dd64-127">Specify the *ResourceGroupName* parameter to get a unique vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dd64-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dd64-128">-ResourceGroupName</span></span>
<span data-ttu-id="4dd64-129">指定此 Cmdlet 取得備份保存庫的 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4dd64-129">Specifies the name of an Azure resource group in which this cmdlet gets a Backup vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dd64-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dd64-130">-DefaultProfile</span></span>
<span data-ttu-id="4dd64-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4dd64-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4dd64-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dd64-132">CommonParameters</span></span>
<span data-ttu-id="4dd64-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4dd64-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dd64-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4dd64-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dd64-135">輸入</span><span class="sxs-lookup"><span data-stu-id="4dd64-135">INPUTS</span></span>

## <span data-ttu-id="4dd64-136">輸出</span><span class="sxs-lookup"><span data-stu-id="4dd64-136">OUTPUTS</span></span>

### <span data-ttu-id="4dd64-137">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="4dd64-137">AzureRmBackupVault</span></span>

## <span data-ttu-id="4dd64-138">筆記</span><span class="sxs-lookup"><span data-stu-id="4dd64-138">NOTES</span></span>
* <span data-ttu-id="4dd64-139">所有</span><span class="sxs-lookup"><span data-stu-id="4dd64-139">None</span></span>

## <span data-ttu-id="4dd64-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="4dd64-140">RELATED LINKS</span></span>

[<span data-ttu-id="4dd64-141">AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="4dd64-141">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="4dd64-142">新-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="4dd64-142">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="4dd64-143">移除-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="4dd64-143">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)

[<span data-ttu-id="4dd64-144">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="4dd64-144">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


