---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8CE8F4E9-93D4-41E5-8B43-F886C018D9FB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06681544df4974a1ee906552af96302698e88d74
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966976"
---
# <span data-ttu-id="9cc8f-101">Get-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="9cc8f-101">Get-AzureVMSqlServerExtension</span></span>

## <span data-ttu-id="9cc8f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9cc8f-102">SYNOPSIS</span></span>
<span data-ttu-id="9cc8f-103">取得特定虛擬機器上的 SQL Server IaaS 代理程式的設定。</span><span class="sxs-lookup"><span data-stu-id="9cc8f-103">Gets the settings of the SQL Server IaaS Agent on a particular virtual machine.</span></span>

## <span data-ttu-id="9cc8f-104">句法</span><span class="sxs-lookup"><span data-stu-id="9cc8f-104">SYNTAX</span></span>

```
Get-AzureVMSqlServerExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9cc8f-105">說明</span><span class="sxs-lookup"><span data-stu-id="9cc8f-105">DESCRIPTION</span></span>
<span data-ttu-id="9cc8f-106">**AzureVMSqlServerExtension** Cmdlet 會取得 SQL Server 基礎結構的設定，做為特定虛擬機器上的服務 (IaaS) 代理程式。</span><span class="sxs-lookup"><span data-stu-id="9cc8f-106">The **Get-AzureVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a particular virtual machine.</span></span>

## <span data-ttu-id="9cc8f-107">示例</span><span class="sxs-lookup"><span data-stu-id="9cc8f-107">EXAMPLES</span></span>

### <span data-ttu-id="9cc8f-108">範例1：在虛擬機器上取得 SQL Server 延伸設定</span><span class="sxs-lookup"><span data-stu-id="9cc8f-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureVMSqlServerExtension-VM $VM
          ExtensionName        : SqlIaaSAgent
          Publisher            : Microsoft.SqlServer.Management
          Version              : 1.0
          State                : Enable
          RoleName             : VMName
          AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
          AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="9cc8f-109">取得特定虛擬機器上的 SQL Server 延伸設定。</span><span class="sxs-lookup"><span data-stu-id="9cc8f-109">Gets the settings of the SQL Server extension on a particular virtual machine.</span></span>

### <span data-ttu-id="9cc8f-110">範例2：在虛擬機器上取得 SQL Server IaaS 代理程式的設定</span><span class="sxs-lookup"><span data-stu-id="9cc8f-110">Example 2: Get the settings of a SQL Server IaaS Agent on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "Service" -Name "VMName" | Get-AzureVMSqlServerExtension
          ExtensionName        : SqlIaaSAgent
          Publisher            : Microsoft.SqlServer.Management
          Version              : 1.0
          State                : Enable
          RoleName             : VMName
          AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
          AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="9cc8f-111">使用管道輸入來取得特定虛擬機器上的 SQL Server IaaS 代理程式設定。</span><span class="sxs-lookup"><span data-stu-id="9cc8f-111">Gets the settings of the SQL Server IaaS Agent on a particular virtual machine using piped input.</span></span>

### <span data-ttu-id="9cc8f-112">範例3：在虛擬機器上取得特定 SQL Server 版本 IaaS 代理程式的設定</span><span class="sxs-lookup"><span data-stu-id="9cc8f-112">Example 3: Get the settings of specific SQL Server version IaaS Agent on a virtual machine</span></span>
```
PS C:\> Get-AzureVMSqlServerExtension -VM $VM -Version "1.0"
          ExtensionName        : SqlIaaSAgent
          Publisher            : Microsoft.SqlServer.Management
          Version              : 1.0
          State                : Enable
          RoleName             : VMName
          AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
          AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="9cc8f-113">這個命令會取得虛擬機器上特定版本的 SQL Server IaaS 代理程式的設定。</span><span class="sxs-lookup"><span data-stu-id="9cc8f-113">This command gets the settings of the particular version of SQL Server IaaS Agent on a virtual machine.</span></span>

## <span data-ttu-id="9cc8f-114">參數</span><span class="sxs-lookup"><span data-stu-id="9cc8f-114">PARAMETERS</span></span>

### <span data-ttu-id="9cc8f-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9cc8f-115">-InformationAction</span></span>
<span data-ttu-id="9cc8f-116">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="9cc8f-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9cc8f-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="9cc8f-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9cc8f-118">持續</span><span class="sxs-lookup"><span data-stu-id="9cc8f-118">Continue</span></span>
- <span data-ttu-id="9cc8f-119">理會</span><span class="sxs-lookup"><span data-stu-id="9cc8f-119">Ignore</span></span>
- <span data-ttu-id="9cc8f-120">看</span><span class="sxs-lookup"><span data-stu-id="9cc8f-120">Inquire</span></span>
- <span data-ttu-id="9cc8f-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9cc8f-121">SilentlyContinue</span></span>
- <span data-ttu-id="9cc8f-122">停止</span><span class="sxs-lookup"><span data-stu-id="9cc8f-122">Stop</span></span>
- <span data-ttu-id="9cc8f-123">封存</span><span class="sxs-lookup"><span data-stu-id="9cc8f-123">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cc8f-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9cc8f-124">-InformationVariable</span></span>
<span data-ttu-id="9cc8f-125">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="9cc8f-125">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cc8f-126">-設定檔</span><span class="sxs-lookup"><span data-stu-id="9cc8f-126">-Profile</span></span>
<span data-ttu-id="9cc8f-127">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="9cc8f-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9cc8f-128">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="9cc8f-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cc8f-129">-VM</span><span class="sxs-lookup"><span data-stu-id="9cc8f-129">-VM</span></span>
<span data-ttu-id="9cc8f-130">指定此 Cmdlet 取得設定的持久性虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="9cc8f-130">Specifies the persistent virtual machine object that this cmdlet gets settings from.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cc8f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cc8f-131">CommonParameters</span></span>
<span data-ttu-id="9cc8f-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9cc8f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cc8f-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9cc8f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cc8f-134">輸入</span><span class="sxs-lookup"><span data-stu-id="9cc8f-134">INPUTS</span></span>

## <span data-ttu-id="9cc8f-135">輸出</span><span class="sxs-lookup"><span data-stu-id="9cc8f-135">OUTPUTS</span></span>

## <span data-ttu-id="9cc8f-136">筆記</span><span class="sxs-lookup"><span data-stu-id="9cc8f-136">NOTES</span></span>

## <span data-ttu-id="9cc8f-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="9cc8f-137">RELATED LINKS</span></span>

[<span data-ttu-id="9cc8f-138">移除-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="9cc8f-138">Remove-AzureVMSqlServerExtension</span></span>](./Remove-AzureVMSqlServerExtension.md)

[<span data-ttu-id="9cc8f-139">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="9cc8f-139">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)


